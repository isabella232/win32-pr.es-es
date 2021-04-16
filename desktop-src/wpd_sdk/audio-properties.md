---
description: Los dispositivos portátiles de Windows admiten las siguientes propiedades de audio.
ms.assetid: 5d6c6a95-abb7-4191-a961-bcb30ca96bb6
title: Propiedades de audio (PortableDevice. h)
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
ms.openlocfilehash: 1bdab201fc987d5bc1aff3638fbb57358115fdce
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699407"
---
# <a name="audio-properties"></a>Propiedades de audio

Los dispositivos portátiles de Windows admiten las siguientes propiedades de audio.



| Propiedad                         | VarType     | Descripción                                                                                                                                                                                                        |
|----------------------------------|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_profundidad de \_ bits de audio de WPD \_**       | **VT \_ UI4** | La profundidad de bits del audio.                                                                                                                                                                                        |
| **velocidad de bits de \_ audio WPD \_**          | **VT \_ UI4** | Velocidad de bits del audio, en bits por segundo.                                                                                                                                                                     |
| **\_alineación del \_ bloque de audio de WPD \_** | **VT \_ UI4** | La alineación de bloque del archivo de audio, en bytes.                                                                                                                                                                   |
| **recuento de canales de audio de WPD \_ \_ \_**   | **VT \_ R4**  | El número de canales de este archivo de audio, por ejemplo, 1, 2 o 5,1.                                                                                                                                              |
| **\_código de \_ formato de audio de WPD \_**     | **VT \_ UI4** | Número de código del formato de onda registrado. Para obtener una lista de formatos de onda registrados, consulte el artículo [registro de códigos FourCC y formatos de onda](https://msdn2.microsoft.com/library/ms867195.aspx) en el sitio web de MSDN. |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Propiedades y atributos de WPD**](properties-and-attributes.md)
</dt> </dl>

 

 




