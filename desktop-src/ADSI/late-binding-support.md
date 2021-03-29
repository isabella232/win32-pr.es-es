---
title: Compatibilidad con enlace en tiempo de ejecución
description: Cuando la compatibilidad con enlace en tiempo de ejecución está en su lugar, cada llamada de función debe pasar por la interfaz IDispatch de ADSI, antes de redirigirse a la extensión adecuada.
ms.assetid: fbdc6234-9381-4d64-bf02-05e393b3e0bd
ms.tgt_platform: multiple
keywords:
- extensiones ADSI, compatibilidad con enlace en tiempo de ejecución
- ADSI ADSI, Visual Basic de código de ejemplo, compatibilidad con enlaces en tiempo de ejecución
- enlace de AD, compatibilidad con enlace en tiempo de ejecución
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0e4dd1de0000d9edbe3e73cbc47b81d094d48c2
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "103793882"
---
# <a name="late-binding-support"></a>Compatibilidad con enlace en tiempo de ejecución

Cuando la compatibilidad con enlace en tiempo de ejecución está en su lugar, cada llamada de función debe pasar por la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) de ADSI, antes de redirigirse a la extensión adecuada.

Tenga en cuenta el siguiente código de ejemplo.


```C++
Set x = GetObject("LDAP://CN=JeffSmith, OU=Sales, 
                   DC=Fabrikam,DC=COM")
x.SetPassword("newPassword")
 
 
x.MyNewMethod( "\\srv\public")
x.MyProperty = "Hello World"
 
x.OtherMethod()
x.OtherProperty = 4362
 
Debug.Print x.LastName
```



No hay llamadas explícitas al método **QueryInterface** para obtener las extensiones. Las extensiones deben redirigir sus llamadas [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) a la interfaz **IDispatch** de ADSI. ADSI toma la decisión y resuelve los conflictos que se producen, después vuelve a enrutar a la extensión adecuada mediante una interfaz denominada [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension). Por lo tanto, cualquier extensión que admita el enlace en tiempo de ejecución debe implementar **IADsExtension**.

 

 