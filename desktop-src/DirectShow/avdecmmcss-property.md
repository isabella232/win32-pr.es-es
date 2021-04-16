---
description: Especifica la clase del servicio Programador de clases multimedia (MMCSS) para el subproceso de descodificación.
ms.assetid: 77724879-62e4-439e-9dd0-3642cd7f75ca
title: Propiedad AVDecMmcss (UUID. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0092ac516f9600929a9772d044f51e7e375548d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671624"
---
# <a name="avdecmmcss-property"></a>Propiedad AVDecMmcss

Especifica la clase del servicio Programador de clases multimedia (MMCSS) para el subproceso de descodificación.

Esta propiedad es de lectura y escritura.

## <a name="data-type"></a>Tipo de datos

**BSTR** (**VT \_ BSTR**)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVDecMmcssClass**

## <a name="property-value"></a>Valor de propiedad

El valor de esta propiedad es el nombre de la clase MMCSS.

## <a name="remarks"></a>Observaciones

MMCSS permite a las aplicaciones asegurarse de que el procesamiento dependiente del tiempo ha priorizado el acceso a los recursos de la CPU. Funciona mediante la elevación de subprocesos registrados a prioridades de subprocesos mayores, a la vez que reduce periódicamente sus prioridades para dar tiempo a otros procesos.

El valor recomendado para los descodificadores de audio es "audio", y el valor recomendado para los descodificadores de vídeo es "reproducción".

Si el servicio MMCSS no está disponible o la clase de MMCSS especificada no existe, el establecimiento de la propiedad no tiene ningún efecto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>UUID. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Propiedades de la API de códec](codec-api-properties.md)
</dt> <dt>

[**Interfaz ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




