---
title: Atributos de texto predefinidos (TsAttrid. h)
description: Los valores siguientes identifican los atributos de texto obtenidos con el método ITfContext GetAppProperty. Se incluyen el formato de datos y el contenido de cada tipo de propiedad.
ms.assetid: af73edb8-b706-40e4-a093-4ac22d33ecdc
keywords:
- Atributos de texto predefinidos marco de trabajo de servicios de texto
topic_type:
- apiref
api_name:
- Predefined Text Attributes
api_location:
- TsAttrid.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6cb214f6c555b589c52e9916325e38b46b0bfb88
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150853"
---
# <a name="predefined-text-attributes"></a>Atributos de texto predefinidos

Los valores siguientes identifican los atributos de texto obtenidos con el método [**ITfContext:: GetAppProperty**](/windows/desktop/api/msctf/nf-msctf-itfcontext-getappproperty) . Se incluyen el formato de datos y el contenido de cada tipo de propiedad.

## <a name="properties"></a>Propiedades



| Propiedad                                     | Descripción                                                                                                                                              |
|----------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_Texto TSATTRID                               | No se utiliza.                                                                                                                                                |
| \_Alineación del texto TSATTRID \_                    | No se utiliza.                                                                                                                                                |
| TSATTRID \_ \_ centro de alineación de texto \_            | Contiene un valor distinto de cero si el texto está centrado o cero en caso contrario.                                                                                      |
| TSATTRID \_ \_ justificación de alineación de texto \_           | Contiene un valor distinto de cero si el texto está justificado o cero en caso contrario.                                                                                     |
| Alineación de texto a la TSATTRID \_ \_ \_ izquierda              | Contiene un valor distinto de cero si el texto está alineado a la izquierda o a cero en caso contrario.                                                                                  |
| TSATTRID \_ alineación de texto \_ \_ derecha             | Contiene un valor distinto de cero si el texto está alineado a la derecha o cero en caso contrario.                                                                                 |
| TSATTRID \_ Text \_ EmbeddedObject               | Contiene un valor distinto de cero si el texto es un objeto incrustado o cero en caso contrario.                                                                            |
| TSATTRID \_ \_ guiones de texto                  | Contiene un valor distinto de cero si el texto se divide en guiones o cero de lo contrario.                                                                                    |
| TSATTRID \_ idioma de texto \_                     | Contiene el identificador de idioma **LANGID** del texto.                                                                                                 |
| \_Vínculo de texto de TSATTRID \_                         | Contiene un puntero a un objeto de vínculo. El autor de la llamada debe usar el método QueryInterface para obtener la interfaz deseada, como **IUniformResourceLocator**. |
| TSATTRID \_ orientación del texto \_                  | Especifica el ángulo, en décimas de grado, entre la línea base de texto y el eje x del dispositivo.                                                          |
| TSATTRID \_ texto \_ para                         | No se utiliza.                                                                                                                                                |
| Texto de TSATTRID \_ \_ para \_ FirstLineIndent        | Contiene el número de puntos que se aplica sangría a la primera línea de un párrafo.                                                                            |
| TSATTRID \_ Text \_ para \_ LeftIndent             | Contiene el número de puntos en los que se aplica la sangría del párrafo a la izquierda.                                                                              |
| TSATTRID \_ texto \_ para \_ LineSpacing            | No se utiliza.                                                                                                                                                |
| TSATTRID \_ texto \_ para \_ LineSpacing al \_ menos   | Contiene el número mínimo de líneas para el interlineado del párrafo.                                                                              |
| TSATTRID el \_ texto \_ para \_ LineSpacing \_ Double    | Contiene un valor distinto de cero si el párrafo tiene un espacio doble o cero en caso contrario.                                                                            |
| TSATTRID \_ texto \_ para \_ LineSpacing \_ exactamente   | Contiene el número exacto de líneas para el interlineado del párrafo.                                                                                |
| TSATTRID texto para la mayoría de la \_ \_ \_ LineSpacing \_  | Contiene el número de líneas para el espaciado de líneas múltiples del párrafo.                                                                             |
| TSATTRID \_ Text \_ para \_ LineSpacing \_ OnePtFive | Contiene un valor distinto de cero si el párrafo es una línea o una media, o bien cero, de lo contrario.                                                             |
| TSATTRID \_ texto \_ para \_ la \_ línea única    | Contiene un valor distinto de cero si el párrafo tiene un solo espacio o cero en caso contrario.                                                                            |
| TSATTRID \_ texto \_ para \_ RightIndent            | Contiene el número de puntos a los que se aplica la sangría del párrafo a la derecha.                                                                             |
| TSATTRID \_ texto \_ para \_ SpaceAfter             | Contiene el número de puntos de espaciado después del párrafo.                                                                                            |
| TSATTRID \_ Text \_ para \_ SpaceBefore            | Contiene el número de puntos del espaciado antes del párrafo.                                                                                           |
| TSATTRID \_ texto de \_ solo lectura                     | Contiene cero si el texto es de solo lectura o distinto de cero en caso contrario.                                                                                             |
| TSATTRID \_ texto \_ RightToLeft                  | Contiene cero si el texto se lee de derecha a izquierda o es distinto de cero en caso contrario.                                                                                 |
| TSATTRID \_ Text \_ VerticalWriting              | Especifica si el texto es vertical u horizontal. Contiene cero si el texto es horizontal o es distinto de cero si el texto es vertical.                             |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                            |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                  |
| Redistribuible<br/>          | TSF 1,0 en Windows 2000 Professional<br/>                                       |
| Encabezado<br/>                   | <dl> <dt>TsAttrid. h</dt> </dl> |



 

