---
description: shujiajia Pro API V1.0
---

# API

### 接口列表

{service}为标注平台实际部署实例地址，访问时不需要带上端口。

<table><thead><tr><th width="83">序号</th><th width="227">接口名称</th><th width="331">请求路径</th><th>请求方式</th></tr></thead><tbody><tr><td>1</td><td>数据集创建</td><td>{service}/api/v1/datasets</td><td>POST</td></tr><tr><td>2</td><td>查询数据集列表</td><td>{service}/api/v1/datasets</td><td>GET</td></tr><tr><td>3</td><td>查询数据集详情</td><td>{service}/api/v1/datasets/{dataset-id}</td><td>GET</td></tr><tr><td>4</td><td>删除数据集</td><td>{service}/api/v1/datasets/{dataset-id}</td><td>DELETE</td></tr><tr><td>5</td><td>更新数据集</td><td>{service}/api/v1/datasets</td><td>PATCH</td></tr><tr><td>6</td><td>数据集上传</td><td>{service}/api/v1/datasets/{dataset-id}/batchs</td><td>POST</td></tr><tr><td>7</td><td>数据集上传进度查询</td><td>{service}/api/v1/datasets/process/{upload-id}</td><td>GET</td></tr><tr><td>8</td><td>数据集下载</td><td>{service}/api/v1/datasets/exports</td><td>POST</td></tr><tr><td>9</td><td>数据集下载进度查询</td><td>{service}/api/v1/datasets/exports/{export-id}</td><td>GET</td></tr><tr><td>10</td><td>获取任务列表</td><td>{service}/api/v1/tasks</td><td>GET</td></tr><tr><td>11</td><td>任务创建（复制）</td><td>{service}/api/v1/tasks</td><td>POST</td></tr><tr><td>12</td><td>任务详情查询</td><td>{service}/api/v1/tasks/task-id</td><td>GET</td></tr><tr><td>13</td><td>任务标注结果导出</td><td>{service}/api/v1/exports</td><td>POST</td></tr><tr><td>14</td><td>任务标注结果导出进度查询</td><td>{service}/api/v1/exports/{export-id}</td><td>GET</td></tr></tbody></table>

### 术语说明

<table><thead><tr><th width="100">序号</th><th width="137">术语</th><th>说明</th></tr></thead><tbody><tr><td>1</td><td>任务</td><td><p>标注的组织形式，通过一个既存的任务复制创建一个新的任务。 在标注平台管理后台对一个任务的创建，需要如下要素，缺一不可： </p><p>• 归属项目</p><p>• 基本信息 </p><p>• 模板工具 </p><p>• 使用流程 </p><p>• 执行团队</p></td></tr><tr><td>2</td><td>数据集</td><td>标注平台的数据组织形式，一个任务只能关联绑定一个数据集。</td></tr><tr><td>3</td><td>数据集批次</td><td>一个数据集可包含多个批次，批次可以简单类比数据集的一个根目录。</td></tr><tr><td>4</td><td>任务状态</td><td><p>任务状态包括四种：</p><p>• 未开始：任务未创建完毕，未开始状态的任务无法进行标注。</p><p>• 进行中：任务标注中。</p><p>• 暂停中：因某些特定原因，管理员可通过管理后台将任务设定为“暂停中”，该状态下，标注活动暂停，不能进行标注、质检和验收工作。</p><p>• 已完成：管理员在任务列表中，通过“操作”中的“完成”按钮手动将该任务置为“已完成”时的任务状态，此状态代表项目经理确认该标注任务完成，可以将该任务标注结果导出。</p></td></tr><tr><td>5</td><td>文件导出地址</td><td>是指客户端将标注文件导出到标注平台以外的地址进行存储。使用标注平台外部导出地址时，需要确保标注平台与外部文件存储地址的网络连通性。</td></tr></tbody></table>

