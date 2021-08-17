---
description: Hay varias consultas interesantes en un controlador que una aplicación puede realizar si no hay ningún costo de rendimiento.
ms.assetid: 81e1c5c5-03bc-4598-814e-14e56513e221
title: Notificación asincrónica (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbd23a64e613bbbae56154dc35c05bcf08b75c4c91f306360153e775e12c40ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119123422"
---
# <a name="asynchronous-notification-direct3d-9"></a>Notificación asincrónica (Direct3D 9)

Hay varias consultas interesantes en un controlador que una aplicación puede realizar si no hay ningún costo de rendimiento. En Direct3D 7 y Direct3D 8, un mecanismo de consulta sincrónico, GetInfo, funcionaba bien para cosas como estadísticas, pero no se agregaban consultas críticas para el rendimiento. Hay otras cosas (como las barreras) que son intrínsecamente asincrónicas. Se trata de una API sencilla para realizar consultas sincrónicas y asincrónicas. GetInfo se retirará en Direct3D 9.

Cree una consulta [**mediante IDirect3DDevice9::CreateQuery**](/windows/desktop/api). Este método toma un D3DQUERYTYPE, que define el tipo de consulta que se va a realizar y devuelve un puntero a un [**objeto IDirect3DQuery9.**](/windows/desktop/api) Si no se admite el tipo de consulta, la llamada devuelve un error D3DERR \_ NOTAVAILABLE. Con el objeto de consulta, la aplicación envía la consulta al tiempo de ejecución mediante [**IDirect3DQuery9::Issue**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-issue)y sondea el estado de la consulta mediante [**IDirect3DQuery9::GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata). Si el resultado de la consulta está disponible, se devuelve S \_ OK; de lo contrario, se devuelve S \_ FALSE. Se espera que la aplicación pase un búfer con el tamaño adecuado para los resultados de la consulta.

La aplicación tiene una opción para forzar al tiempo de ejecución a vaciar la consulta en el controlador mediante D3DGETDATA FLUSH con \_ [**IDirect3DQuery9::GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata). Provoca un vaciado, lo que obliga al controlador a ver la consulta. En este caso, se devuelve D3DERR \_ DEVICELOST si el dispositivo se pierde.

Todas las consultas se pierden cuando se pierde el dispositivo, la aplicación tiene que volver a crearlas. Si el dispositivo no admite la consulta y pQueryID es **NULL,** se producirá un error en la creación de la consulta con D3DERR \_ INVALIDCALL.

En la tabla siguiente se resume información importante sobre cada tipo de consulta.



| QuertyType                    | Marca de problema válida              | Búfer GetData              | Tiempo de ejecución      | Inicio implícito de la consulta |
|-------------------------------|-------------------------------|-----------------------------|--------------|-----------------------------|
| D3DQUERYTYPE \_ VCACHE          | D3DISSUE \_ END                 | D3DDEVINFO \_ VCACHE          | Retail/Debug | CreateDevice                |
| D3DQUERYTYPE \_ ResourceManager | D3DISSUE \_ END                 | D3DDEVINFO \_ ResourceManager | Solo depuración   | Presente                     |
| D3DQUERYTYPE \_ VERTEXSTATS     | D3DISSUE \_ END                 | D3DDEVINFO \_ D3DVERTEXSTATS  | Solo depuración   | Presente                     |
| EVENTO D3DQUERYTYPE \_           | D3DISSUE \_ END                 | BOOL                        | Retail/Debug | CreateDevice                |
| OCLUSIÓN DE D3DQUERYTYPE \_       | D3DISSUE \_ BEGIN,D3DISSUE \_ END | DWORD                       | Retail/Debug | N/D                         |



 

Campo Marcas para [**IDirect3DQuery9::Issue**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-issue):


```
#define D3DISSUE_END (1 << 0) 
// Tells the runtime to issue the end of a query, changing its state to 
//   "non-signaled" 
```




```
 
#define D3DISSUE_BEGIN (1 << 1) // Tells the runtime to issue the 
// beginning of a query. 
```



Campo Flags para [**IDirect3DQuery9::GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata):


```
 
#define D3DGETDATA_FLUSH (1 << 0) // Tells the runtime to flush 
// if the query is outstanding.
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Programación Sugerencias](programming-tips.md)
</dt> </dl>

 

 
