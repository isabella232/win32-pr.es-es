---
description: Contiene el objeto de scripting para la vista.
ms.assetid: 63a4e42f-3d24-493f-8801-fc09a7477401
title: Propiedad ShellFolderView. script (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderView.Script
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 86926f2013dd78c2c6685163ae78f890c337a251
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278497"
---
# <a name="shellfolderviewscript-property"></a>Propiedad ShellFolderView. script

\[Esta propiedad no se admite en Windows XP o posterior.\]

Contiene el objeto de scripting para la vista.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
objScript = ShellFolderView.Script
```



## <a name="property-value"></a>Valor de propiedad

Variable de tipo [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) que recibe el objeto de scripting.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]<br/>                                         |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                           |
| Encabezado<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                           |
| IDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                         |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 4,71 o posterior)</dt> </dl> |



 

 
