---
description: 'Método Product.SourceListAddMediaDisk: el método SourceListAddMediaDisk agrega un disco al conjunto de discos registrados. Acepta Diskid, VolumeLabel y DiskPrompt como parámetros. Este método llama a en MsiSourceListAddMediaDisk.'
ms.assetid: 19cb6884-2191-4da3-a6d2-8874564be67d
title: Método Product.SourceListAddMediaDisk
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.SourceListAddMediaDisk
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 9e3f6df653abeefd57f8311eed0d9e578f6a525c1a0dc915f4b629d367bb79fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120042135"
---
# <a name="productsourcelistaddmediadisk-method"></a>Método Product.SourceListAddMediaDisk

El **método SourceListAddMediaDisk** agrega un disco al conjunto de discos registrados. Acepta *Diskid,* *VolumeLabel* y *DiskPrompt como* parámetros. Este método llama a [**en MsiSourceListAddMediaDisk**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddmediadiska).

## <a name="syntax"></a>Sintaxis


```JScript
Product.SourceListAddMediaDisk(
  Diskid,
  VolumeLabel,
  DiskPrompt
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Diskid* 
</dt> <dd>

Este parámetro proporciona el identificador del disco que se va a agregar o actualizar.

</dd> <dt>

*VolumeLabel* 
</dt> <dd>

Este parámetro proporciona la etiqueta del disco que se va a agregar o actualizar. Una actualización sobrescribe la etiqueta de volumen existente en el Registro. Para cambiar solo el símbolo del sistema del disco, obtenga la etiqueta de volumen registrada existente y proséntala junto con el nuevo símbolo del sistema de disco. Una cadena vacía para este parámetro registra una cadena vacía (0 bytes de longitud) como etiqueta de volumen.

</dd> <dt>

*DiskPrompt* 
</dt> <dd>

Este parámetro proporciona el símbolo del sistema del disco que se va a agregar o actualizar. Una actualización sobrescribe el mensaje de disco existente en el Registro. Para cambiar solo la etiqueta de volumen, obtenga el mensaje de disco existente del registro y proporcione la nueva etiqueta de volumen. Una cadena vacía para este parámetro registra una cadena vacía (0 bytes de longitud) como símbolo del sistema del disco.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Instalador 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador 3.0 o posterior en Windows Server 2003, Windows XP y Windows 2000<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID IProduct se define como \_ 000C10A0-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Producto**](product-object.md)
</dt> <dt>

[**MsiSourceListAddMediaDisk**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddmediadiska)
</dt> <dt>

[No se admite en Windows Installer 2.0 y versiones anteriores](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




