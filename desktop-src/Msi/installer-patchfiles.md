---
description: La propiedad PatchFiles devuelve un objeto StringList que contiene una lista de archivos que se pueden actualizar mediante la lista de revisiones proporcionada.
ms.assetid: 14549847-8558-4a9a-9ad5-3575c3f4391e
title: Installer.PatchFiles, propiedad
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.PatchFiles
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: a71386be84982545a15dcc9b8b9f6456d60c6fad7bb3e40310d65d067a54bf19
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119810995"
---
# <a name="installerpatchfiles-property"></a>Installer.PatchFiles, propiedad

La **propiedad PatchFiles** devuelve un [**objeto StringList**](stringlist-object.md) que contiene una lista de archivos que se pueden actualizar mediante la lista de revisiones proporcionada. Esta propiedad llama [**a MsiGetPatchFileList.**](/windows/desktop/api/Msi/nf-msi-msigetpatchfilelista) Para obtener más información sobre el uso de **la propiedad PatchFiles,** vea [Enumerar los archivos que se pueden actualizar.](listing-the-files-that-can-be-updated.md)

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
propVal = Installer.PatchFiles
```



## <a name="property-value"></a>Valor de propiedad

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Instalador 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador 4.5 en Windows Server 2003 y Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                           |
| IID<br/>     | IID IInstaller se define como \_ 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                                |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Installer (objeto)**](installer-object.md)
</dt> <dt>

[No se admite en Windows Installer 3.1 y versiones anteriores](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




