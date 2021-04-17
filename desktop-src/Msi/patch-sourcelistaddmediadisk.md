---
description: El método SourceListAddMediaDisk agrega un disco al conjunto de discos registrados. Acepta dipatine, VolumeLabel y DiskPrompt como parámetros. Este método llama a en MsiSourceListAddMediaDisk.
ms.assetid: 6feaf2d3-7e39-4e22-9e74-9a2f98369eac
title: Patch. SourceListAddMediaDisk (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.SourceListAddMediaDisk
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: a7c74ccdfb90a0cb365e6110defc9b60dac1f471
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653691"
---
# <a name="patchsourcelistaddmediadisk-method"></a>Patch. SourceListAddMediaDisk (método)

El método **SourceListAddMediaDisk** agrega un disco al conjunto de discos registrados. Acepta *dipatine*, *VolumeLabel* y *DiskPrompt* como parámetros. Este método llama a en [**MsiSourceListAddMediaDisk**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddmediadiska).

## <a name="syntax"></a>Sintaxis


```JScript
Patch.SourceListAddMediaDisk(
  Diskid,
  VolumeLabel,
  DiskPrompt
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Detectaron* 
</dt> <dd>

Este parámetro proporciona el identificador del disco que se va a agregar o actualizar.

</dd> <dt>

*VolumeLabel* 
</dt> <dd>

Este parámetro proporciona la etiqueta del disco que se va a agregar o actualizar. Una actualización sobrescribe la etiqueta de volumen existente en el registro. Para cambiar solo la solicitud de disco, obtenga la etiqueta de volumen registrada existente y proporcione el nuevo símbolo del sistema. Una cadena nula o vacía registra una cadena vacía (0 bytes de longitud) como etiqueta de volumen.

</dd> <dt>

*DiskPrompt* 
</dt> <dd>

Este parámetro proporciona el símbolo del sistema del disco que se va a agregar o actualizar. Una actualización sobrescribe el mensaje de disco existente en el registro. Para cambiar solo la etiqueta de volumen, obtenga el aviso de disco existente del registro y proporcione la nueva etiqueta de volumen. Una cadena nula o vacía registra una cadena vacía (0 bytes de longitud) como el símbolo del sistema.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer 3,0 o posterior en Windows Server 2003, Windows XP y Windows 2000<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID \_ IPatch se define como 000C10A1-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                            |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Distribución**](patch-object.md)
</dt> <dt>

[**MsiSourceListAddMediaDisk**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddmediadiska)
</dt> <dt>

[No se admite en Windows Installer 2,0 y versiones anteriores](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




