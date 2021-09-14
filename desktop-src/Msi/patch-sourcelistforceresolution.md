---
description: El método SourceListForceResolution borra la última propiedad de origen usada.
ms.assetid: 9ecfdf6e-4fed-46fc-8956-85d20cbe5327
title: Patch.SourceListForceResolution (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.SourceListForceResolution
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: f9a44d08c05b4ece24cf3c8c8d3be42e210aec32
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127173693"
---
# <a name="patchsourcelistforceresolution-method"></a>Patch.SourceListForceResolution (método)

El **método SourceListForceResolution** borra la última propiedad de origen usada. Esto obliga al instalador a buscar en la lista de origen un origen de revisión válido la próxima vez que se requiera el origen de la revisión. Por ejemplo, el instalador requiere que el origen de la revisión realice una instalación o reinstalación cuando falta la copia de caché local de la revisión. Este método llama a [**MsiSourceListForceResolution.**](/windows/desktop/api/Msi/nf-msi-msisourcelistforceresolutiona)

## <a name="syntax"></a>Sintaxis


```JScript
Patch.SourceListForceResolution()
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador 3.0 o posterior en Windows Server 2003, Windows XP y Windows 2000<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID IPatch se define como \_ 000C10A1-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                            |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Parche**](patch-object.md)
</dt> <dt>

[**MsiSourceListForceResolution**](/windows/desktop/api/Msi/nf-msi-msisourcelistforceresolutiona)
</dt> <dt>

[No se admite en Windows Installer 2.0 y versiones anteriores](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




