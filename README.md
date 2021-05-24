# Code Snippets for MyStock

This is the README for extension "code-snippets-for-mystock".

## Installation

- 打开 VSCode
- 拓展中心搜索 "Code Snippets for MyStock"
- 点击安装

## Features
- Code Snippets 代码快速生成

## Snippets
- Code Snippets 命令以简洁、易懂为主
- Code Snippets 中注释说明以 MyStock 则为代码片段

### api
| 快捷 | 描述 |
| --- | --- |
| api.get | 快速生成 api get 请求 Code Snippets |
| api.post | 快速生成 api post 请求 Code Snippets |
| api.put | 快速生成 api put 请求 Code Snippets |
| api.delete | 快速生成 api delete 请求 Code Snippets |

```javascript
/**
 * 获取
 * @api-url xxx
 */
export const  = (params?: any) => {
  const apiUrl = '';
  return request.get(apiUrl, { params });
};

/**
 * 提交
 * @api-url xxx
 */
export const  = (params?: any) => {
  const apiUrl = '';
  return request.post(url, { ...params });
};

/**
 * 删除
 * @api-url xxx
 */
export const  = (params?: any) => {
  const apiUrl = '';
  return request.delete(url, { data: params });
};

/**
 * put数据
 * @api-url xxx
 */
export const  = (params?: any) => {
  const apiUrl = '';
  return request.put(apiUrl, { ...params });
};
```

### hooks
| 快捷 | 描述 |
| --- | --- |
| state | 快速生成一个hook state Code Snippets |
| loading | 快速生成一个hook loading state Code Snippets |
| firstRender | 快速生成一个hook firstRender state Code Snippets |
| loadFailed | 快速生成一个hook loadFailed state Code Snippets |
| fll | 快速生成三个hook firstRender、loadFailed、loading state Code Snippets |
| quit | 快速生成两个hook quitPath quitComfirmed Code Snippets |

```javascript
// state
const [state, setState] = React.useState();
// firstRender
const [firstRender, setFirstRender] = React.useState(true);
// loading
const [loading, setLoading] = React.useState(false);
// loadFailed
const [loadFailed, setLoadFailed] = React.useState(true);
// fll
const [firstRender, setFirstRender] = React.useState(true);
const [loadFailed, setLoadFailed] = React.useState(true);
const [loading, setLoading] = React.useState(false);
// quit
let promptExecuted = false;
const [quitPath, setQuitPath] = React.useState('');
const [quitComfirmed, setQuitComfirmed] = React.useState(false);
```

### react
| 快捷 | 描述 |
| --- | --- |
| template | 快速生成 React 模板 Code Snippets |
| template.child | 快速生成 React 模板（带props） Code Snippets |
| page-list | 快速生成列表页整体框架 page-list Code Snippets |
| pro-table | 快速生成表格 pro-table Code Snippets |
| quit-modal | 快速生成quit模态框 quit-modal Code Snippets |
| modal | 快速生成模态框normal-modal Code Snippets |
| mass-tool | 快速生成mass-tool Code Snippets |
| es-search | 快速生成es-search Code Snippets |
| select-input-option | 快速生成select-input-option Code Snippets |
| select-input | 快速生成select-input Code Snippets |
| card | 快速生成card Code Snippets |
| bread-crumb | 快速生成bread-crumb Code Snippets |
| tabs | 快速生成tabs Code Snippets |
| tabs-status | 快速生成tabs-status Code Snippets |
| text-status | 快速生成text-status Code Snippets |
| upload | 快速生成upload Code Snippets |


```javascript
/*** template ***/
/* eslint-disable no-unused-expressions */
/* eslint-disable react-hooks/exhaustive-deps */
import {
  React,
  useTranslate,
} from '@/utils/require';
import './index.less';

const index: React.FC = () => {
  const translate = useTranslate();

  React.useEffect(() => {
  }, []);

  return (
    <div>
      {translate('1')}
    </div>
  );
};
export default index;
```
```javascript
/*** template.child ***/
/* eslint-disable no-unused-expressions */
/* eslint-disable react-hooks/exhaustive-deps */
import {
  React,
  useTranslate,
} from '@/utils/require';
import './index.less';

interface PropsTypes {
  params: any;
}
const index: React.FC<PropsTypes> = (props) => {
  const { params }: any = props;
  const translate = useTranslate();

  React.useEffect(() => {
  }, []);

  return (
    <div>
      {translate('1')}
    </div>
  );
};
export default index;
```
```javascript
/*** template.page-list ***/
/* eslint-disable no-unused-expressions */
/* eslint-disable react-hooks/exhaustive-deps */
import {
  React,
  Page,
  rowClickable,
  ColumnType,
  ProTable,
  useTranslate,
} from '@/utils/require';
import './index.less';

interface PropsTypes {
  params: any;
}
const index: React.FC<PropsTypes> = (props) => {
  const { params }: any = props;
  const translate = useTranslate();

  const columns: ColumnType[] = [
    {
      title: translate(''),
      width: 100,
      dataIndex: ''
    },
    {
      title: translate(''),
      width: 100,
      dataIndex: ''
    },
    {
      title: translate(''),
      width: 100,
      dataIndex: ''
    },
    {
      title: translate(''),
      width: 100,
      dataIndex: ''
    },
    {
      title: translate(''),
      width: 100,
      dataIndex: ''
    },
    {
      title: translate('action'),
      width: 100,
      dataIndex: ''
      render:() => (<div>1</div>)
    },
];

  React.useEffect(() => {
  }, []);

  return (
    <Page>
      <div>
        <Page.Header>
          <Page.Title sub_title={translate('')}>
            {translate('')}
          </Page.Title>
        </Page.Header>
        <Page.Filters>
        </Page.Filters>
        <ProTable
          rowKey=''
          stickyParentSelector='.basic-layout-content > div > div'
          columns={columns}
          request={}
          searchModel={}
          emptyText={translate('')}
          rowClickable
          showQuickJumper
          onRow={record => ({
          onClick: (event: any) => {
            if (rowClickable(event)) {

              }
            }
           })}
        />
      </div>
    </Page>
  );
};
export default index;

```
```javascript
/*** pro-table ***/
<ProTable
  rowKey=''
  stickyParentSelector='.basic-layout-content > div > div'
  columns={columns}
  request={}
  searchModel={}
  emptyText={translate('')}
  rowClickable
  showQuickJumper
  onRow={record => ({
  onClick: (event: any) => {
    if (rowClickable(event)) {

      }
    }
   })}
/>

```
```javascript
/*** quit-modal ***/
<Prompt
  when={!quitComfirmed}
  message={(location) => {
    if (!promptExecuted && location.pathname !== '/login') {
      promptExecuted = true;
      Modal.confirm({
        icon: null,
        centered: true,
        closable: true,
        closeIcon: <CloseIcon />,
        title: `${translate('quit')}`,
        content: translate(''),
        okText: translate('quit'),
        cancelText: translate(''),
        onOk: () => {
          const url = '';
          setQuitPath(url);
          setQuitComfirmed(true);
        },
      });
      setTimeout(() => {
        promptExecuted = false;
      }, 500);
    }
    return false;
  }}
 >
```
```javascript
/*** columns ***/
const columns = [
  {
    title: translate(''),
    width: 160,
    dataIndex: '',
   },
   {
     title: translate(''),
     width: 160,
     dataIndex: '',
     render: (val: any, record: any) => {
       // TO DO
     }
    },
   {
     title: translate(''),
     hint: translate(''),
     width: 160,
     dataIndex: '',
     sorter: {
       key: '',
       multiple: 1
     },
   }
 ];

```
```javascript
/*** modal ***/
<Modal
  wrapClassName=''
  visible={visible}
  title={translate('')}
  width={}
  okText={translate('')}
  cancelText={translate('')}
  onOk={_ => {
    // TO DO
  }}
  onCancel={_ => {
    // TO DO
  }}
>
  <div> 1 </div>
</Modal>
```
```javascript
/*** mass-tool ***/
<MassToolBar
  message=''
  selectedCount={selectedCount}
  maxCount={maxCount}
  viewSelected={}
>
  <Tooltip title={!selectedCount ? translate('please_select_at_least_1_product_first') : null}>
    <Button
      disabled={!selectedCount}
      onClick={}
    >
      {translate('')}
    </Button>
  </Tooltip>
</MassToolBar>
```
```javascript
/*** es-search ***/
<div className=''>
  <span className=''>
    {translate('')}
  </span>
  <EsSearch
    url=''
    esDocName=''
    onSelect={(value: any) => {
     // TO DO
    }}
    onChange={(value: any) => {
     // TO DO
    }}
    onPressEnter={(value: any) => {
     // TO DO
    }}
  />
</div>
```
```javascript
/*** select-input-option ***/
const inputCommonProps = {
  style: { width: 360 },
  placeholder: translate('input'),
};
const selectOptions: SelectOption[] = [
  {
    name: translate(''),
    value: '',
    extraProps: {
      ...inputCommonProps,
      esDocName: '',
      url: '',
    },
    type: 'esSearch',
  },
  {
    name: translate(''),
    value: '',
    extraProps: inputCommonProps,
  },
  {
    name: translate(''),
    value: '',
    extraProps: inputCommonProps,
  }
]
```
```javascript
/*** select-input ***/
<SelectInput
  selectOptions={selectOptions}
  onChange={(value: any) =>{}}
  onPressEnter={(value: any) =>{}}
  onEsSearchSelect={(value: any) =>{}}
  onSelect={(key: any) => {}}
  selectProps={{
    defaultValue: '',
    style: { width: 360 },
  }}
/>
```
```javascript
/*** cards ***/
<Card bordered={false}>
  <div className='card-title'>
    {translate('basic_info')}
  </div>
  <section>
    // TO DO
  </section>
</Card>
```
```javascript
/*** bread-crumb ***/
<Breadcrumb>
  <Breadcrumb.Item>
    <Link to=''>{translate('')}</Link>
  </Breadcrumb.Item>
  <Breadcrumb.Item>
    {translate('')}
  </Breadcrumb.Item>
</Breadcrumb>
```
```javascript
/*** tabs ***/
<Tabs
  activeKey={tabKey}
  onChange={changeTab}
  animated={false}
  className=''
>
  <Tabs.TabPane tab={translate('')} key='1'>
    // todo
  </Tabs.TabPane>
  <Tabs.TabPane tab={translate('')} key='2'>
    // todo
  </Tabs.TabPane>
</Tabs>
```
```javascript
/*** tabs-status ***/
<Tabs onChange={changeTab} type='card' defaultActiveKey={tabKey}>
  <TabPane tab={`${translate('Pending')} pendingAccount`} key='1'>
    {tabKey === '1' ? renderTable() : null}
  </TabPane>
  <TabPane tab={translate('Done')} key='2'>
    {tabKey === '2' ? renderTable() : null}
  </TabPane>
  <TabPane tab={translate('Cancelled')} key='9'>
    {tabKey === '9' ? renderTable() : null}
  </TabPane>
</Tabs>
```
```javascript
/*** test-status ***/
<TextStatus text={translate('main')} type='green' />
```
```javascript
/*** upload ***/
<SimpleUploadArea
  accept='.xlsx,.xls'
  beforeUploadText={translate('')}
  uploadRequest={uploadRequest}
  userGuideSlot={userGuideSlot}
  loading={!!batchTasks.length || uploading}
  disabledHint={translate('')}
/> 
```

**Enjoy!**
