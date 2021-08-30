---
description: La propiedad Context devuelve el contexto de esta revisión.
ms.assetid: 09c92b0b-44f3-4355-8171-03da8ba32757
title: Patch.Context, propiedad
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.Context
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 3316c71c5de15a777ce7e4559b7ee52e9efcb61200bd72b8898440e56bb4f392
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120042425"
---
# <a name="patchcontext-property"></a>Patch.Context, propiedad

La **propiedad Context** devuelve el contexto de esta revisión.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
propVal = Patch.Context
```



## <a name="property-value"></a>Valor de propiedad

## <a name="remarks"></a>Comentarios

Esta propiedad devuelve uno de los valores siguientes.



| Context                        | Value | Significado                        |
|--------------------------------|-------|--------------------------------|
| MSIINSTALLCONTEXT \_ USERMANAGED | 1     | Revisión en contexto administrado.   |
| USUARIO \_ MSIINSTALLCONTEXT        | 2     | Revisión en contexto no administrado. |
| MÁQUINA \_ MSIINSTALLCONTEXT     | 4     | Revisión en el contexto de la máquina.   |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Instalador 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador 3.0 o posterior en Windows Server 2003, Windows XP y Windows 2000<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID IPatch se define como \_ 000C10A1-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                            |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Patch (objeto)**](patch-object.md)
</dt> <dt>

[No se admite en Windows Installer 2.0 y versiones anteriores](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




