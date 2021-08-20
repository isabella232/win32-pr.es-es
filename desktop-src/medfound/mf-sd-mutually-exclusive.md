---
description: Especifica si una secuencia es mutuamente excluyente con otras secuencias del mismo tipo.
ms.assetid: 00a426ae-297c-4fcb-8132-d9c538bc9f1a
title: MF_SD_MUTUALLY_EXCLUSIVE atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed57e4acccb4c15684e583c1bcb18b68c850644fe59121e7fda31acbd6181503
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117691700"
---
# <a name="mf_sd_mutually_exclusive-attribute"></a>Atributo MF \_ SD \_ MUTUALLY \_ EXCLUSIVE

Especifica si una secuencia es mutuamente excluyente con otras secuencias del mismo tipo.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame [**a IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para establecer este atributo, llame [**a IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Se aplica a

[**IMFStreamDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)

## <a name="remarks"></a>Comentarios

Si este atributo es **TRUE** (distinto de cero), la secuencia se excluye mutuamente con otras secuencias del mismo tipo, como audio o vídeo, dentro de la misma presentación. Por ejemplo, si un archivo AVI contiene varias secuencias de audio, se marcan como mutuamente excluyentes, ya que solo se debe reproducir una secuencia de audio a la vez.

El valor predeterminado es **FALSE**.

> [!Note]  
> Este atributo no se usa para los archivos de formato de sistemas avanzados (ASF), que tienen una manera más sofisticada de representar criterios de exclusión mutua. Para obtener más información, [**vea IMFASFMutualExclusion**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfmutualexclusion).

 

La constante GUID para este atributo se exporta desde mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio \| para UWP\]<br/>                                  |
| Servidor mínimo compatible<br/> | Windows Aplicaciones de escritorio para \[ UWP de Server 2008 R2 \|\]<br/>                     |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos del descriptor de flujo](stream-descriptor-attributes.md)
</dt> </dl>

 

 




