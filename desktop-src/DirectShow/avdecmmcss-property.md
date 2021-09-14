---
description: Especifica la clase Servicio programador de clases multimedia (MMCSS) para el subproceso decoding.
ms.assetid: 77724879-62e4-439e-9dd0-3642cd7f75ca
title: Propiedad AVDecMmcss (Uuids.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0092ac516f9600929a9772d044f51e7e375548d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127162121"
---
# <a name="avdecmmcss-property"></a>Propiedad AVDecMmcss

Especifica la clase Servicio programador de clases multimedia (MMCSS) para el subproceso decoding.

Esta propiedad es de lectura y escritura.

## <a name="data-type"></a>Tipo de datos

**BSTR** (**VT \_ BSTR**)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVDecMmcssClass**

## <a name="property-value"></a>Valor de propiedad

El valor de esta propiedad es el nombre de la clase MMCSS.

## <a name="remarks"></a>Observaciones

MMCSS permite a las aplicaciones asegurarse de que el procesamiento con límite de tiempo ha priorizado el acceso a los recursos de CPU. Funciona elevando los subprocesos registrados a prioridades de subprocesos más altas, a la vez que disminuye periódicamente sus prioridades para dar tiempo a otros procesos.

El valor recomendado para los descodificadores de audio es "Audio" y el valor recomendado para los descodificadores de vídeo es "Playback".

Si el servicio MMCSS no está disponible o la clase MMCSS especificada no existe, establecer la propiedad no tiene ningún efecto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Uuids.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades de la API de códec](codec-api-properties.md)
</dt> <dt>

[**ICodecAPI (interfaz)**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




