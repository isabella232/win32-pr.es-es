---
description: Windows Dispositivos portátiles admite las siguientes propiedades de audio.
ms.assetid: 5d6c6a95-abb7-4191-a961-bcb30ca96bb6
title: Propiedades de audio (PortableDevice.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Audio
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 93ddbee0eb078c1b9d5a1e7c64288e95b47e2bdb0363bf8b7b19cb773129d0ba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119590415"
---
# <a name="audio-properties"></a>Propiedades de audio

Windows Dispositivos portátiles admite las siguientes propiedades de audio.



| Propiedad                         | VarType     | Descripción                                                                                                                                                                                                        |
|----------------------------------|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **PROFUNDIDAD DE \_ BITS DE \_ AUDIO \_ WPD**       | **VT \_ UI4** | Profundidad de bits del audio.                                                                                                                                                                                        |
| **VELOCIDAD DE \_ BITS DE AUDIO \_ WPD**          | **VT \_ UI4** | Velocidad de bits del audio, en bits por segundo.                                                                                                                                                                     |
| **ALINEACIÓN DE \_ BLOQUES DE AUDIO \_ WPD \_** | **VT \_ UI4** | Alineación de bloques del archivo de audio, en bytes.                                                                                                                                                                   |
| **RECUENTO DE \_ CANALES DE AUDIO \_ \_ WPD**   | **VT \_ R4**  | El número de canales de este archivo de audio, por ejemplo, 1, 2 o 5.1.                                                                                                                                              |
| **CÓDIGO DE \_ FORMATO DE AUDIO \_ \_ WPD**     | **VT \_ UI4** | Número de código de formato WAVE registrado. Para obtener una lista de los formatos WAVE registrados, consulte el artículo [Códigos FOURCC](https://msdn2.microsoft.com/library/ms867195.aspx) registrados y formatos WAVE en el sitio web de MSDN. |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Propiedades y atributos de WPD**](properties-and-attributes.md)
</dt> </dl>

 

 




