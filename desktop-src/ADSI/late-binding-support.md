---
title: Compatibilidad con enlaces en tiempo de tarde
description: Cuando se dispone de compatibilidad con el enlace en tiempo de tarde, cada llamada de función debe pasar por la interfaz ADSI IDispatch, antes de que se vuelva a enrutar a la extensión adecuada.
ms.assetid: fbdc6234-9381-4d64-bf02-05e393b3e0bd
ms.tgt_platform: multiple
keywords:
- extensiones ADSI, compatibilidad con enlaces en tiempo de tarde
- ADSI ADSI, código de ejemplo Visual Basic compatibilidad con enlaces en tiempo de tarde
- enlace de AD, compatibilidad con enlaces en tiempo de tarde
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0e4dd1de0000d9edbe3e73cbc47b81d094d48c2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126970415"
---
# <a name="late-binding-support"></a>Compatibilidad con enlaces en tiempo de tarde

Cuando se dispone de compatibilidad con el enlace en tiempo de tarde, cada llamada de función debe pasar por la interfaz [**ADSI IDispatch,**](/windows/win32/api/oaidl/nn-oaidl-idispatch) antes de que se vuelva a enrutar a la extensión adecuada.

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



No hay llamadas explícitas al **método QueryInterface** para llegar a las extensiones. Las extensiones deben redirigir sus llamadas [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) a la interfaz **ADSI IDispatch.** ADSI toma la decisión y resuelve los conflictos que se producen y, a continuación, vuelve a enrutar a la extensión adecuada mediante una interfaz denominada [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension). Por lo tanto, cualquier extensión que admita el enlace en tiempo de ejecución debe implementar **IADsExtension**.

 

 