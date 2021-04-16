---
title: Objetos incrustados (marco de trabajo de servicios de texto)
description: El marco de trabajo de servicios de texto permite que un servicio de texto inserte objetos en una secuencia de texto de la aplicación.
ms.assetid: 44cb22b5-707b-4f21-b986-5258ed273543
keywords:
- Text Services Framework (TSF), objetos incrustados
- TSF (marco de trabajo de servicios de texto), objetos incrustados
- Aplicaciones habilitadas para TSF, objetos incrustados
- objetos incrustados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39e4f819e6f42cc4e8d2ed81e47c79efe5ff7407
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104571374"
---
# <a name="embedded-objects-text-services-framework"></a>Objetos incrustados (marco de trabajo de servicios de texto)

El marco de trabajo de servicios de texto permite que un servicio de texto inserte objetos en una secuencia de texto de la aplicación. Los objetos incrustados se insertan en la secuencia de texto mediante el valor de [carácter de TS \_ \_ incrustado](ts-char--constants.md). Este valor se resuelve como el carácter de reemplazo del objeto Unicode U + fffc, mediante la notación hexadecimal. Por ejemplo, en la siguiente ilustración se muestra la representación de un objeto incrustado que representa el ideograma japonés *HI*, en combinación con la secuencia de caracteres Unicode que representan la traducción en Inglés de "Sun".

![codificación de caracteres de un objeto incrustado](images/emb-obj.gif)

La fila superior de la ilustración contiene el texto traducido, que consta de la palabra "Sun" seguida del carácter japonés de Sun, *HI*. La fila central de la ilustración muestra el carácter Unicode. En el caso de U + fffc, este es el carácter de reemplazo de objeto. La fila inferior de la ilustración muestra el valor hexadecimal de cada carácter.

## <a name="supporting-embedded-objects-in-an-application"></a>Compatibilidad de objetos incrustados en una aplicación

El administrador de TSF inserta un objeto incrustado en la secuencia de texto mediante una llamada a [ITextStoreACP:: InsertEmbedded](/windows/desktop/api/textstor/nf-textstor-itextstoreacp-insertembedded) para una aplicación basada en ACP, o [ITextStoreAnchor:: InsertEmbedded](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-insertembedded) para una aplicación basada en delimitadores. Cuando se inserta un objeto incrustado, la aplicación debe colocar el valor **\_ \_ incrustado de carácter de TS** en la posición de carácter (o ubicación de delimitador) donde se incrusta el objeto y almacenar el IDataObject asociado al objeto incrustado. Cuando se llama a [ITextStoreACP:: gettext](/windows/desktop/api/textstor/nf-textstor-itextstoreacp-gettext) o [ITextStoreAnchor:: gettext](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-gettext) y un objeto incrustado se encuentra dentro del texto obtenido, el valor **\_ \_ incrustado de carácter de TS** indica la presencia y la ubicación del objeto incrustado. Para obtener el objeto incrustado, llame a [ITextStoreACP:: GetEmbedded](/windows/desktop/api/textstor/nf-textstor-itextstoreacp-getembedded) con la posición de carácter del objeto incrustado o [ITextStoreAnchor:: GetEmbedded](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getembedded) con la ubicación de delimitador del objeto incrustado.

Normalmente, la aplicación no reconoce el contenido del objeto incrustado. La aplicación puede intentar obtener información de pantalla del propio objeto. Si el objeto incrustado puede proporcionar datos en un formato reconocido por la aplicación, como el \_ mapa de bits UNICODETEXT o CF \_ , la aplicación puede mostrar información gráfica proporcionada por el objeto.

## <a name="inserting-embedded-objects"></a>Insertar objetos incrustados

Un servicio de texto inserta un objeto incrustado en un contexto mediante una llamada a [ITfRange:: InsertEmbedded](/windows/desktop/api/msctf/nf-msctf-itfrange-insertembedded) o [ITfInsertAtSelection:: InsertEmbeddedAtSelection](/windows/desktop/api/msctf/nf-msctf-itfinsertatselection-insertembeddedatselection). El servicio de texto debe proporcionar la IDataObject incrustada.

 

 
