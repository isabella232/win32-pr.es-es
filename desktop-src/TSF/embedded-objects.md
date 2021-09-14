---
title: Objetos incrustados (Text Services Framework)
description: Text Services Framework permite a un servicio de texto insertar objetos en un flujo de texto de aplicación.
ms.assetid: 44cb22b5-707b-4f21-b986-5258ed273543
keywords:
- Text Services Framework (TSF), objetos incrustados
- TSF (Text Services Framework), objetos incrustados
- Aplicaciones habilitadas para TSF, objetos incrustados
- objetos incrustados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39e4f819e6f42cc4e8d2ed81e47c79efe5ff7407
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127243656"
---
# <a name="embedded-objects-text-services-framework"></a>Objetos incrustados (Text Services Framework)

Text Services Framework permite a un servicio de texto insertar objetos en un flujo de texto de aplicación. Los objetos incrustados se insertan en la secuencia de texto con el [valor TS \_ CHAR \_ EMBEDDED](ts-char--constants.md). Este valor se resuelve en el carácter de reemplazo de objetos Unicode U+fffc, utilizando la notación hexadecimal. Por ejemplo, en la ilustración siguiente se muestra la representación de un objeto incrustado que representa el ideograma *japonés hi*, en combinación con la secuencia de caracteres Unicode que representan la traducción al inglés de "Sun".

![codificación de caracteres de un objeto incrustado](images/emb-obj.gif)

La fila superior de la ilustración contiene el texto traducido, que consta de la palabra "Sun" seguida del carácter japonés para sun, *hi*. La fila central de la ilustración muestra el carácter Unicode. En el caso de U+fffc, este es el carácter de reemplazo del objeto. La fila inferior de la ilustración muestra el valor hexadecimal de cada carácter.

## <a name="supporting-embedded-objects-in-an-application"></a>Admitir objetos incrustados en una aplicación

El administrador de TSF inserta un objeto incrustado en la secuencia de texto mediante una llamada a [ITextStoreACP::InsertEmbedded](/windows/desktop/api/textstor/nf-textstor-itextstoreacp-insertembedded) para una aplicación basada en ACP o [ATextStoreAnchor::InsertEmbedded](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-insertembedded) para una aplicación basada en delimitadores. Cuando se inserta un objeto incrustado, la aplicación debe colocar el valor de **TS \_ CHAR \_ EMBEDDED** en la posición de caracteres (o ubicación del delimitador) donde se incrusta el objeto y almacenar el IDataObject asociado al objeto incrustado. Cuando se llama a [ITextStoreACP::GetText](/windows/desktop/api/textstor/nf-textstor-itextstoreacp-gettext) o [ITextStoreAnchor::GetText](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-gettext) y se incluye un objeto incrustado dentro del texto obtenido, el valor **de TS \_ CHAR \_ EMBEDDED** indica la presencia y la ubicación del objeto incrustado. Para obtener el objeto incrustado, llame a [ITextStoreACP::GetEmbedded con](/windows/desktop/api/textstor/nf-textstor-itextstoreacp-getembedded) la posición de carácter del objeto incrustado o [a ITextStoreAnchor::GetEmbedded](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getembedded) con la ubicación delimitadora del objeto incrustado.

Normalmente, la aplicación no reconoce el contenido del objeto incrustado. La aplicación puede intentar obtener información de visualización del propio objeto. Si el objeto incrustado puede proporcionar datos en un formato que la aplicación reconoce, como CF UNICODETEXT o CF BITMAP, la aplicación puede mostrar información gráfica proporcionada \_ \_ por el objeto .

## <a name="inserting-embedded-objects"></a>Insertar objetos incrustados

Un servicio de texto inserta un objeto incrustado en un contexto mediante una llamada a [ITfRange::InsertEmbedded](/windows/desktop/api/msctf/nf-msctf-itfrange-insertembedded) o [ITfInsertAtSelection::InsertEmbeddedAtSelection](/windows/desktop/api/msctf/nf-msctf-itfinsertatselection-insertembeddedatselection). El servicio de texto debe proporcionar el IDataObject incrustado.

 

 
