---
title: Atributos de fuente predefinidos (TsAttrid.h)
description: Los valores siguientes identifican los atributos de fuente obtenidos con el método GetAppProperty de ITfContext. Se incluyen el formato de datos y el contenido de cada tipo de propiedad.
ms.assetid: 8d73c258-77d5-46db-9d31-ac41d9e7acb3
keywords:
- Atributos de fuente predefinidos Text Services Framework
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
ms.openlocfilehash: 0fb586258bb6eca1639121fa3b33a26ad560f00bb9b002c347a4e026a53442f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117951951"
---
# <a name="predefined-font-attributes"></a>Atributos de fuente predefinidos

Los valores siguientes identifican los atributos de fuente obtenidos [con el método ITfContext::GetAppProperty.](/windows/desktop/api/msctf/nf-msctf-itfcontext-getappproperty) Se incluyen el formato de datos y el contenido de cada tipo de propiedad.

## <a name="properties"></a>Propiedades



| Propiedad                                                 | Descripción                                                                                                                 |
|----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| **Fuente TSATTRID \_**                                       | No se usa.                                                                                                                   |
| **TSATTRID \_ Font \_ FaceName**                             | Contiene el nombre de la cara de la fuente de texto.                                                                                    |
| **TSATTRID \_ Font \_ SizePts**                              | Contiene el tamaño de punto de la fuente de texto.                                                                                   |
| **Estilo de fuente TSATTRID \_ \_**                                | No se usa.                                                                                                                   |
| **Animación de estilo de fuente TSATTRID \_ \_ \_**                     | No se usa.                                                                                                                   |
| **Animación de estilo de fuente TSATTRID \_ \_ \_ \_ BlinkingBackground** | Contiene un valor distinto de cero si el texto tiene la animación especificada o cero en caso contrario.                                         |
| **TSATTRID \_ Font \_ Style \_ Animation \_ LasVegasLights**     | Contiene un valor distinto de cero si el texto tiene la animación especificada o cero en caso contrario.                                         |
| **Animación de estilo de fuente TSATTRID \_ \_ \_ \_ MarchingBlackAnts**  | Contiene un valor distinto de cero si el texto tiene la animación especificada o cero en caso contrario.                                         |
| **Animación de estilo de fuente TSATTRID \_ \_ \_ \_ MarchingRedAnts**    | Contiene un valor distinto de cero si el texto tiene la animación especificada o cero en caso contrario.                                         |
| **TSATTRID \_ Font \_ Style \_ Animation \_ Shimmer**            | Contiene un valor distinto de cero si el texto tiene la animación especificada o cero en caso contrario.                                         |
| **SparkleText de animación de \_ \_ estilo de fuente \_ TSATTRID \_**        | Contiene un valor distinto de cero si el texto tiene la animación especificada o cero en caso contrario.                                         |
| **TSATTRID \_ Font \_ Style \_ Animation \_ WipeDown**           | Contiene un valor distinto de cero si el texto tiene la animación especificada o cero en caso contrario.                                         |
| **TSATTRID \_ Font \_ Style \_ Animation \_ WipeRight**          | Contiene un valor distinto de cero si el texto tiene la animación especificada o cero en caso contrario.                                         |
| **BackgroundColor de estilo \_ de \_ fuente TSATTRID \_**               | Contiene el valor RGB del fondo del texto. Contiene 0xFF000000 si el color del texto es automático.                          |
| **Parpadeo del estilo de fuente TSATTRID \_ \_ \_**                         | Contiene un valor distinto de cero si el texto parpadea o cero de lo contrario.                                                         |
| **Negrita de estilo de fuente TSATTRID \_ \_ \_**                          | Contiene un valor distinto de cero si el texto está en negrita o cero en caso contrario.                                                             |
| **Mayúsculas del estilo de fuente TSATTRID \_ \_ \_**                    | Contiene un valor distinto de cero si el texto está en mayúsculas o cero en caso contrario.                                                      |
| **Color de estilo de fuente TSATTRID \_ \_ \_**                         | Contiene el valor RGB del color del texto. Contiene 0xFF000000 si el color del texto es automático.                               |
| **Relieve de estilo \_ de \_ fuente TSATTRID \_**                        | Contiene un valor distinto de cero si el texto está en relieve o cero en caso contrario.                                                         |
| **TSATTRID \_ Font Style (Estilo de fuente \_ TSATTRID) \_**                       | Contiene un valor distinto de cero si el texto está escrito o cero en caso contrario.                                                         |
| **Alto del estilo de fuente TSATTRID \_ \_ \_**                        | Contiene el alto de fuente. Para obtener más información, vea el **miembro lfHeight** de la estructura LOGFONT.                       |
| **Estilo de fuente TSATTRID \_ \_ \_ oculto**                        | Contiene un valor distinto de cero si el texto está oculto o cero de lo contrario.                                                           |
| **Estilo de fuente TSATTRID \_ \_ \_ Cursiva**                        | Contiene un valor distinto de cero si el texto está en cursiva o cero en caso contrario.                                                           |
| **Kerning de estilo de fuente TSATTRID \_ \_ \_**                       | Contiene el tamaño mínimo de kerning. Para obtener más información, vea ITextFont::GetKerning.                                         |
| **Estilo de fuente TSATTRID \_ \_ en \_ minúsculas**                     | Contiene un valor distinto de cero si el texto está en minúsculas o cero en caso contrario.                                                        |
| **Estilo de fuente TSATTRID \_ \_ \_ descrito**                      | Contiene un valor distinto de cero si se describe el texto o cero en caso contrario.                                                         |
| **Estilo de fuente TSATTRID \_ \_ \_ sobrelineado**                      | Contiene un valor distinto de cero si el texto está sobrelineado o cero en caso contrario.                                                        |
| **Estilo de fuente TSATTRID \_ \_ \_ Overline \_ Double**              | Contiene un valor distinto de cero si el texto se sobrelinea de forma doble o cero en caso contrario.                                                 |
| **Estilo de fuente TSATTRID \_ \_ \_ \_ sobrelineado único**              | Contiene un valor distinto de cero si el texto está sobrelineado o cero de lo contrario.                                                 |
| **Posición del estilo de fuente TSATTRID \_ \_ \_**                      | Contiene la posición de fuente.                                                                                                 |
| **Estilo de fuente TSATTRID \_ \_ \_ protegido**                     | Contiene un valor distinto de cero si el texto está protegido o cero en caso contrario.                                                        |
| **Sombra de estilo de fuente TSATTRID \_ \_ \_**                        | Contiene un valor distinto de cero si el texto se sombrea o cero de lo contrario.                                                         |
| **SmallCaps de \_ estilo de fuente \_ TSATTRID \_**                     | Contiene un valor distinto de cero si el texto está en minúsculas o cero en caso contrario.                                                        |
| **Espaciado de estilo de fuente TSATTRID \_ \_ \_**                       | Contiene el espaciado de fuente.                                                                                                  |
| **TSATTRID \_ Font \_ Style \_ Strikethrough**                 | No se usa.                                                                                                                   |
| **TSATTRID \_ Font \_ Style \_ Strikethrough \_ Double**         | Contiene un valor distinto de cero si el texto es tachado doble o cero en caso contrario.                                             |
| **TSATTRID \_ Font \_ Style \_ Strikethrough \_ Single**         | Contiene un valor distinto de cero si el texto es tachado único o cero en caso contrario.                                             |
| **Subíndice de estilo de fuente TSATTRID \_ \_ \_**                     | Contiene un valor distinto de cero si el texto es subíndice o cero en caso contrario.                                                        |
| **Superíndice de estilo de fuente TSATTRID \_ \_ \_**                   | Contiene un valor distinto de cero si el texto es superíndice o cero de lo contrario.                                                      |
| **Subrayado de estilo de fuente TSATTRID \_ \_ \_**                     | Contiene un valor distinto de cero si el texto está subrayado o cero en caso contrario.                                                       |
| **TSATTRID \_ Font \_ Style \_ Underline \_ Double**             | Contiene un valor distinto de cero si el texto está subrayado doble o cero en caso contrario.                                                |
| **TSATTRID \_ Font \_ Style \_ Underline \_ Single**             | Contiene un valor distinto de cero si el texto está subrayado o cero de lo contrario.                                                |
| **Estilo de fuente TSATTRID \_ \_ en \_ mayúsculas**                     | Contiene un valor distinto de cero si el texto está en mayúsculas o cero en caso contrario.                                                        |
| **Peso del estilo de fuente TSATTRID \_ \_ \_**                        | Contiene el grosor de la fuente. Para obtener más información sobre los valores posibles, vea **el miembro lfWeight** de la estructura LOGFONT. |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                            |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                  |
| Redistribuible<br/>          | TSF 1.0 en Windows 2000 Professional<br/>                                       |
| Header<br/>                   | <dl> <dt>TsAttrid.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ITfContext::GetAppProperty](/windows/desktop/api/msctf/nf-msctf-itfcontext-getappproperty)
</dt> </dl>

 

