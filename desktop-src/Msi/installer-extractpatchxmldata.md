---
description: El método ExtractPatchXMLData del objeto Installer extrae información de una revisión como una cadena XML. La información se puede usar para determinar si la revisión se aplica en un sistema de destino. Este método llama a MsiExtractPatchXMLData.
ms.assetid: 85940940-2002-4cb1-8e29-ba2374bf3796
title: Método Installer.ExtractPatchXMLData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ExtractPatchXMLData
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 69c17236c0a4cd96820e0366df51b28cf47ecfb0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127171665"
---
# <a name="installerextractpatchxmldata-method"></a>Método Installer.ExtractPatchXMLData

El **método ExtractPatchXMLData** del [**objeto Installer**](installer-object.md) extrae información de una revisión como una cadena XML. La información se puede usar para determinar si la revisión se aplica en un sistema de destino. Este método llama [**a MsiExtractPatchXMLData.**](/windows/desktop/api/Msi/nf-msi-msiextractpatchxmldataa)

## <a name="syntax"></a>Sintaxis


```JScript
Installer.ExtractPatchXMLData(
  PatchPath
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*PatchPath* 
</dt> <dd>

Ruta de acceso completa a la revisión de la que se va a extraer la información de aplicabilidad.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Instalador 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador 3.0 o posterior en Windows Server 2003 o Windows XP.<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                    |
| IID<br/>     | IID IInstaller se define como \_ 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                                         |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**MsiExtractPatchXMLData**](/windows/desktop/api/Msi/nf-msi-msiextractpatchxmldataa)
</dt> <dt>

[No se admite en Windows Installer 2.0 y versiones anteriores](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




