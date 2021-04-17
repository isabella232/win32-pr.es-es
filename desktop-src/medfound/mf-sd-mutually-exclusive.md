---
description: Especifica si una secuencia es mutuamente excluyente con otras secuencias del mismo tipo.
ms.assetid: 00a426ae-297c-4fcb-8132-d9c538bc9f1a
title: MF_SD_MUTUALLY_EXCLUSIVE atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24e3604eb9424bb646766f57261f745c57e18f3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716493"
---
# <a name="mf_sd_mutually_exclusive-attribute"></a>\_Atributo de \_ uso mutuamente \_ exclusivo de MF SD

Especifica si una secuencia es mutuamente excluyente con otras secuencias del mismo tipo.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame a [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para establecer este atributo, llame a [**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Se aplica a

[**IMFStreamDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)

## <a name="remarks"></a>Observaciones

Si este atributo es **true** (distinto de cero), la secuencia es mutuamente excluyente con otras secuencias del mismo tipo, como audio o vídeo, dentro de la misma presentación. Por ejemplo, si un archivo AVI contiene varias secuencias de audio, se marcan como mutuamente excluyentes, porque solo debe reproducirse una secuencia de audio al mismo tiempo.

El valor predeterminado es **FALSE**.

> [!Note]  
> Este atributo no se utiliza para los archivos de formato de sistema avanzado (ASF), que tienen una forma más sofisticada de representar criterios de exclusión mutua. Para obtener más información, vea [**IMFASFMutualExclusion**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfmutualexclusion).

 

La constante GUID para este atributo se exporta desde mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows 7 \|\]<br/>                                  |
| Servidor mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 R2 \|\]<br/>                     |
| Encabezado<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de descriptor de secuencia](stream-descriptor-attributes.md)
</dt> </dl>

 

 




