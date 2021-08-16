---
description: El método SourceListClearAll del objeto Patch borra la lista de origen completa de todos los orígenes del tipo especificado para una revisión. Acepta Type como parámetro. Este método llama a MsiSourceListClearAllEx.
ms.assetid: 9458a3db-8eaa-4067-875f-8fac68bdf1f8
title: Patch.SourceListClearAll (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.SourceListClearAll
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: ae7de8c0a830000b3100e84cacbf088fefb592ddaa912a7737a35ea009a3cfe1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118942305"
---
# <a name="patchsourcelistclearall-method"></a>Patch.SourceListClearAll (método)

El **método SourceListClearAll** del objeto [**Patch**](patch-object.md) borra la lista de origen completa de todos los orígenes del tipo especificado para una revisión. Acepta *Type como* parámetro. Este método llama [**a MsiSourceListClearAllEx.**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearallexa)

## <a name="syntax"></a>Sintaxis


```JScript
Patch.SourceListClearAll(
  Type
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Tipo* 
</dt> <dd>

Tipo de origen, como red, dirección URL o medios.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador 3.0 o posterior en Windows Server 2003, Windows XP y Windows 2000<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID IPatch se define como \_ 000C10A1-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                            |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Parche**](patch-object.md)
</dt> <dt>

[**MsiSourceListClearAllEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearallexa)
</dt> <dt>

[No se admite en Windows Installer 2.0 y versiones anteriores](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




