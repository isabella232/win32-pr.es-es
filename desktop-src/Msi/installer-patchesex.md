---
description: La propiedad PatchesEx devuelve un objeto RecordList que enumera la lista de revisiones.
ms.assetid: 14fa0a1b-325c-42b7-b023-cd168e0615cc
title: Propiedad Installer. PatchesEx
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
ms.openlocfilehash: e615a9d17dbf1a40332afc5b49b3c0c5446963ee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653387"
---
# <a name="installerpatchesex-property"></a>Propiedad Installer. PatchesEx

La propiedad **PatchesEx** devuelve un objeto [**RecordList**](recordlist-object.md) que enumera la lista de revisiones. Esta propiedad llama a [**MsiEnumPatchesEx**](/windows/desktop/api/Msi/nf-msi-msienumpatchesexa).

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
propVal = Installer.PatchesEx
```



## <a name="property-value"></a>Valor de propiedad

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer 3,0 o posterior en Windows Server 2003 o Windows XP.<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                    |
| IID<br/>     | IID \_ IInstaller se define como 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                                         |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Instalador**](installer-object.md)
</dt> <dt>

[**MsiEnumPatchesEx**](/windows/desktop/api/Msi/nf-msi-msienumpatchesexa)
</dt> <dt>

[**Distribución**](patch-object.md)
</dt> <dt>

[No se admite en Windows Installer 2,0 y versiones anteriores](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




