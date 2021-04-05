---
title: Atributos de fuente predefinidos (TsAttrid. h)
description: Los valores siguientes identifican los atributos de fuente obtenidos con el método ITfContext GetAppProperty. Se incluyen el formato de datos y el contenido de cada tipo de propiedad.
ms.assetid: 8d73c258-77d5-46db-9d31-ac41d9e7acb3
keywords:
- Atributos de fuente predefinidos marco de trabajo de servicios de texto
topic_type:
- apiref
api_name:
- Predefined Font Attributes
api_location:
- TsAttrid.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21351d790a09c9364a101a62b7516698df154225
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104359794"
---
# <a name="predefined-font-attributes"></a>Atributos de fuente predefinidos

Los valores siguientes identifican los atributos de fuente obtenidos con el método [ITfContext:: GetAppProperty](/windows/desktop/api/msctf/nf-msctf-itfcontext-getappproperty) . Se incluyen el formato de datos y el contenido de cada tipo de propiedad.

## <a name="properties"></a>Propiedades



| Propiedad                                                 | Descripción                                                                                                                 |
|----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| **\_Fuente TSATTRID**                                       | No se utiliza.                                                                                                                   |
| **TSATTRID \_ Font \_ FaceName**                             | Contiene el nombre de la fuente de texto.                                                                                    |
| **TSATTRID \_ Font \_ SizePts**                              | Contiene el tamaño de punto de la fuente del texto.                                                                                   |
| **\_Estilo de fuente TSATTRID \_**                                | No se utiliza.                                                                                                                   |
| **TSATTRID \_ \_ animación de estilo de fuente \_**                     | No se utiliza.                                                                                                                   |
| **TSATTRID \_ animación de estilo de fuente \_ \_ \_ BlinkingBackground** | Contiene un valor distinto de cero si el texto tiene la animación especificada o cero en caso contrario.                                         |
| **TSATTRID \_ animación de estilo de fuente \_ \_ \_ LasVegasLights**     | Contiene un valor distinto de cero si el texto tiene la animación especificada o cero en caso contrario.                                         |
| **TSATTRID \_ animación de estilo de fuente \_ \_ \_ MarchingBlackAnts**  | Contiene un valor distinto de cero si el texto tiene la animación especificada o cero en caso contrario.                                         |
| **TSATTRID \_ animación de estilo de fuente \_ \_ \_ MarchingRedAnts**    | Contiene un valor distinto de cero si el texto tiene la animación especificada o cero en caso contrario.                                         |
| **TSATTRID \_ animación de estilo de fuente \_ \_ \_ Shimmer**            | Contiene un valor distinto de cero si el texto tiene la animación especificada o cero en caso contrario.                                         |
| **TSATTRID \_ animación de estilo de fuente \_ \_ \_ SparkleText**        | Contiene un valor distinto de cero si el texto tiene la animación especificada o cero en caso contrario.                                         |
| **TSATTRID \_ animación de estilo de fuente \_ \_ \_ WipeDown**           | Contiene un valor distinto de cero si el texto tiene la animación especificada o cero en caso contrario.                                         |
| **TSATTRID \_ animación de estilo de fuente \_ \_ \_ WipeRight**          | Contiene un valor distinto de cero si el texto tiene la animación especificada o cero en caso contrario.                                         |
| **\_Estilo de fuente TSATTRID \_ \_ BackgroundColor**               | Contiene el valor RGB del fondo del texto. Contiene 0xFF000000 si el color del texto es automático.                          |
| **\_Estilo de fuente TSATTRID \_ \_ parpadeo**                         | Contiene un valor distinto de cero si el texto parpadea o cero en caso contrario.                                                         |
| **\_Estilo de fuente TSATTRID \_ \_ negrita**                          | Contiene un valor distinto de cero si el texto está en negrita o en cero; en caso contrario, es.                                                             |
| **\_Estilo de fuente TSATTRID \_ \_ mayúscula**                    | Contiene un valor distinto de cero si el texto está en mayúsculas o en cero en caso contrario.                                                      |
| **\_Color de \_ estilo de fuente TSATTRID \_**                         | Contiene el valor RGB del color del texto. Contiene 0xFF000000 si el color del texto es automático.                               |
| **\_Estilo de fuente TSATTRID \_ \_ relieve**                        | Contiene un valor distinto de cero si el texto está en relieve o cero en caso contrario.                                                         |
| **\_Estilo de fuente TSATTRID \_ \_**                       | Contiene un valor distinto de cero si el texto está grabado o cero en caso contrario.                                                         |
| **\_Alto de \_ estilo de fuente de TSATTRID \_**                        | Contiene el alto de la fuente. Para obtener más información, vea el miembro **lfHeight** de la estructura LOGFONT.                       |
| **\_Estilo de fuente TSATTRID \_ \_ oculto**                        | Contiene un valor distinto de cero si el texto está oculto o es cero en caso contrario.                                                           |
| **\_Estilo de fuente TSATTRID \_ \_ cursiva**                        | Contiene un valor distinto de cero si el texto está en cursiva o cero en caso contrario.                                                           |
| **\_ \_ Kerning de estilo de fuente TSATTRID \_**                       | Contiene el tamaño mínimo de interletraje. Para obtener más información, vea ITextFont:: GetKerning.                                         |
| **Estilo de fuente TSATTRID en \_ \_ \_ minúsculas**                     | Contiene un valor distinto de cero si el texto está en minúsculas o cero en caso contrario.                                                        |
| **\_Estilo de fuente TSATTRID \_ \_ descrito**                      | Contiene un valor distinto de cero si el texto se describe o cero en caso contrario.                                                         |
| **TSATTRID \_ \_ línea de estilo de fuente \_**                      | Contiene un valor distinto de cero si el texto está sobrerayado o cero en caso contrario.                                                        |
| **TSATTRID \_ el \_ estilo de fuente \_ \_ doble**              | Contiene un valor distinto de cero si el texto tiene una línea doble o cero en caso contrario.                                                 |
| **\_Estilo de fuente TSATTRID \_ \_ \_**              | Contiene un valor distinto de cero si el texto tiene una línea de subrayado o cero en caso contrario.                                                 |
| **\_Posición del \_ estilo de fuente TSATTRID \_**                      | Contiene la posición de la fuente.                                                                                                 |
| **\_Estilo de fuente TSATTRID \_ \_ protegido**                     | Contiene un valor distinto de cero si el texto está protegido o cero en caso contrario.                                                        |
| **\_Sombra de \_ estilo de fuente TSATTRID \_**                        | Contiene un valor distinto de cero si el texto está sombreado o cero en caso contrario.                                                         |
| **\_Estilo de fuente TSATTRID \_ \_ SmallCaps**                     | Contiene un valor distinto de cero si el texto está en minúsculas o cero en caso contrario.                                                        |
| **\_ \_ Espaciado de estilo de fuente TSATTRID \_**                       | Contiene el espaciado de fuentes.                                                                                                  |
| **\_ \_ Tachado de estilo de fuente TSATTRID \_**                 | No se utiliza.                                                                                                                   |
| **\_ \_ \_ Doble tachado de estilo de fuente TSATTRID \_**         | Contiene un valor distinto de cero si el texto tiene doble tachado o cero en caso contrario.                                             |
| **\_Estilo de fuente TSATTRID \_ \_ tachado \_ único**         | Contiene un valor distinto de cero si el texto tiene un tachado único o cero en caso contrario.                                             |
| **\_Subíndice de \_ estilo de fuente TSATTRID \_**                     | Contiene un valor distinto de cero si el texto es subíndice o cero en caso contrario.                                                        |
| **\_ \_ Superíndice estilo de fuente TSATTRID \_**                   | Contiene un valor distinto de cero si el texto es Superscript o cero en caso contrario.                                                      |
| **TSATTRID \_ el \_ estilo de fuente \_ subrayado**                     | Contiene un valor distinto de cero si el texto está subrayado o cero en caso contrario.                                                       |
| **\_Estilo de \_ fuente \_ subrayado \_ doble TSATTRID**             | Contiene un valor distinto de cero si el texto está doble de subrayado o cero en caso contrario.                                                |
| **\_Estilo de fuente TSATTRID \_ \_ subrayado \_ único**             | Contiene un valor distinto de cero si el texto tiene un solo subrayado o cero en caso contrario.                                                |
| **Estilo de fuente TSATTRID en \_ \_ \_ mayúsculas**                     | Contiene un valor distinto de cero si el texto está en mayúsculas o cero en caso contrario.                                                        |
| **\_Grosor del \_ estilo de fuente TSATTRID \_**                        | Contiene el espesor de la fuente. Para obtener más información sobre los valores posibles, vea el miembro **lfWeight** de la estructura LOGFONT. |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                            |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                  |
| Redistribuible<br/>          | TSF 1,0 en Windows 2000 Professional<br/>                                       |
| Encabezado<br/>                   | <dl> <dt>TsAttrid. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ITfContext::GetAppProperty](/windows/desktop/api/msctf/nf-msctf-itfcontext-getappproperty)
</dt> </dl>

 

