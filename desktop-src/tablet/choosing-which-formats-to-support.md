---
description: El tipo de aplicación que se crea determina qué formato de persistencia de entrada de lápiz se va a admitir.
ms.assetid: bd0a4382-f014-4f03-990d-d2f96aa76ab8
title: Elección de los formatos que se admitirán
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8b8b2197c37db603388a4191e08114800aaba37ee8e89803c7ddfb08be18d3e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120111005"
---
# <a name="choosing-which-formats-to-support"></a>Elección de los formatos que se admitirán

El tipo de aplicación que se crea determina qué formato de persistencia de entrada de lápiz se va a admitir.

## <a name="single-ink-object-applications"></a>Aplicaciones de objeto de entrada manuscrita única

Las aplicaciones cuyos documentos contienen solo entrada manuscrita deben usar el formato serializado de entrada de lápiz (ISF). Deben poder copiar y pegar Ink Serialized Format (ISF). Un ejemplo de esto es una aplicación para dibujar o anotación. Estas aplicaciones pueden usar los [**métodos ClipboardCopy**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clipboardcopy)y [**ClipboardPaste.**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clipboardpaste)

## <a name="complex-applications"></a>Aplicaciones complejas

Las aplicaciones cuyos documentos contienen otro contenido, como texto, deben copiar HTML con archivos Formato de intercambio de gráficos (GIF) notificados, además de ISF. La aplicación debe generar el propio HTML, aunque las interfaces de programación de aplicaciones (API) de Tablet PC generan archivos GIF. Estas aplicaciones también deben poder copiar y pegar ISF para la interoperabilidad con las aplicaciones descritas anteriormente.

## <a name="rtf"></a>RTF

Una aplicación debe ser capaz de generar el formato de texto enriquecido (RTF) si se requiere interoperabilidad con Microsoft Word 2002 u otras aplicaciones heredadas.

## <a name="mime-support"></a>Compatibilidad con MIME

En la tabla siguiente se enumeran los encabezados y extensiones de archivo MIME (Multipurpose Internet Mail Extensions) sugeridos para la entrada de lápiz que se conserva en los archivos mediante ISF o GIF. Estos valores se encuentran en la [**enumeración PersistenceFormat.**](/windows/desktop/api/msinkaut/ne-msinkaut-inkpersistenceformat)



| Formato de persistencia            | Encabezado MIME                                                                                    | Extensión de archivo            |
|-------------------------------|------------------------------------------------------------------------------------------------|---------------------------|
| **Base64Gif**                 | Content-Type: application/x-ms-ink Content-Transfer-Encoding: base64<br/>                | No aplicable<br/> |
| **Base64InkSerializedFormat** | Content-Type: Content-Type: image/gif; format=ink Content-Transfer-Encoding: base64<br/> | No aplicable<br/> |
| **Gif**                       | Content-Type: application/x-ms-ink<br/>                                                  | .gif<br/>           |
| **InkSerializedFormat**       | Content-Type: Content-Type: image/gif; format=ink<br/>                                   | .isf<br/>           |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**PersistenceFormat (Enumeración)**](/windows/desktop/api/msinkaut/ne-msinkaut-inkpersistenceformat)
</dt> </dl>

 

 




