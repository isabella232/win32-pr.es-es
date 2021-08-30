---
description: La propiedad PatchesEx devuelve un objeto RecordList que enumera la lista de revisiones.
ms.assetid: 14fa0a1b-325c-42b7-b023-cd168e0615cc
title: Installer.PatchesEx, propiedad
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.PatchesEx
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: a3d5a2413b61d7f54ed26eefcf17e1a4cd7a98b9bc4dc485b11daf349343f0e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120043665"
---
# <a name="installerpatchesex-property"></a>Installer.PatchesEx, propiedad

La **propiedad PatchesEx** devuelve un [**objeto RecordList**](recordlist-object.md) que enumera la lista de revisiones. Esta propiedad llama [**a MsiEnumPatchesEx.**](/windows/desktop/api/Msi/nf-msi-msienumpatchesexa)

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
propVal = Installer.PatchesEx
```



## <a name="property-value"></a>Valor de propiedad

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador 3.0 o posterior en Windows Server 2003 o Windows XP.<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                    |
| IID<br/>     | IInstaller de IID se define como \_ 000C1090-0000-0000-C000-00000000046<br/>                                                                                                                                                                                         |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Instalador**](installer-object.md)
</dt> <dt>

[**MsiEnumPatchesEx**](/windows/desktop/api/Msi/nf-msi-msienumpatchesexa)
</dt> <dt>

[**Parche**](patch-object.md)
</dt> <dt>

[No se admite en Windows Installer 2.0 y versiones anteriores](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




