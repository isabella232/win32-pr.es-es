---
description: El tipo de aplicación que cree indica el formato de persistencia de la tinta que se va a admitir.
ms.assetid: bd0a4382-f014-4f03-990d-d2f96aa76ab8
title: Elección de los formatos admitidos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 891fa1c21dd3178e925deab27525afa7fa70fa22
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279185"
---
# <a name="choosing-which-formats-to-support"></a>Elección de los formatos admitidos

El tipo de aplicación que cree indica el formato de persistencia de la tinta que se va a admitir.

## <a name="single-ink-object-applications"></a>Aplicaciones de objetos de entrada de lápiz única

Las aplicaciones cuyos documentos contienen solo entradas de lápiz deben usar el formato serializado de entrada de lápiz (ISF). Deberían poder copiar y pegar el formato serializado de entrada de lápiz (ISF). Un ejemplo de esto es una aplicación para dibujar o anotar. Estas aplicaciones pueden usar los métodos [**ClipboardCopy**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clipboardcopy)y [**ClipboardPaste**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clipboardpaste) .

## <a name="complex-applications"></a>Aplicaciones complejas

Las aplicaciones cuyos documentos contienen otro tipo de contenido, como texto, deben copiar HTML con los archivos de formato de intercambio de gráficos enriquecido (GIF), además del ISF. La aplicación debe generar el código HTML, aunque las interfaces de programación de aplicaciones (API) de Tablet PC generan archivos GIF. Estas aplicaciones también deben ser capaces de copiar y pegar el ISF para la interoperabilidad con las aplicaciones descritas anteriormente.

## <a name="rtf"></a>RTF

Una aplicación debe ser capaz de generar un formato de texto enriquecido (RTF) si se requiere interoperabilidad con Microsoft Word 2002 u otras aplicaciones heredadas.

## <a name="mime-support"></a>Compatibilidad con MIME

En la tabla siguiente se enumeran los encabezados de extensiones multipropósito de correo Internet (MIME) y las extensiones de archivo para entradas de lápiz que se conservan en archivos mediante el ISF o GIF. Estos valores se encuentran en la enumeración [**PersistenceFormat**](/windows/desktop/api/msinkaut/ne-msinkaut-inkpersistenceformat) .



| Formato de persistencia            | Encabezado MIME                                                                                    | Extensión de archivo            |
|-------------------------------|------------------------------------------------------------------------------------------------|---------------------------|
| **Base64Gif**                 | Content-Type: application/x-MS-Ink Content-Transfer-Encoding: Base64<br/>                | No aplicable<br/> |
| **Base64InkSerializedFormat** | Content-Type: Content-Type: image/gif; formato = contenido de tinta-transferencia-codificación: Base64<br/> | No aplicable<br/> |
| **GIF**                       | Tipo de contenido: aplicación/x-MS-Ink<br/>                                                  | .gif<br/>           |
| **InkSerializedFormat**       | Content-Type: Content-Type: image/gif; formato = tinta<br/>                                   | . ISF<br/>           |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Enumeración PersistenceFormat**](/windows/desktop/api/msinkaut/ne-msinkaut-inkpersistenceformat)
</dt> </dl>

 

 




