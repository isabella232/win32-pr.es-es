---
title: Acerca del proceso de conversión
description: Acerca del proceso de conversión
ms.assetid: 147b82fd-9e82-4acf-8f8a-43eb02e99024
keywords:
- Reproductor de Windows Media,proceso de conversión
- Reproductor de Windows Media complementos, conversión
- complementos, conversión
- complementos de conversión, proceso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4555c0175da6e08a581f1ac02188b2029054cf587ee5933218524fed667625fb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119903325"
---
# <a name="about-the-conversion-process"></a>Acerca del proceso de conversión

Después Reproductor de Windows Media crear una instancia del complemento de conversión, el proceso continúa de la siguiente manera:

1.  El reproductor llama [a IWMPConvert::ConvertFile](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpconvert-convertfile).
2.  El complemento convierte el archivo proporcionado en el *parámetro bstrInputFile* en un formato ASF.
3.  Si se produce un error en la conversión por algún motivo, el complemento devuelve un código de error adecuado y el proceso se detiene.
4.  Si la conversión se realiza correctamente, el complemento coloca el archivo convertido en la carpeta proporcionada en el parámetro *bstrDestinationFolder* y devuelve la ruta de acceso completa al archivo convertido a través del *parámetro pbstrOutputFile.*
5.  El complemento devuelve un código correcto de **ConvertFile**.
6.  El reproductor copia el archivo convertido en una carpeta de la jerarquía de carpetas music del usuario. El lugar exacto en el que el reproductor copia el archivo depende del contenido. Como parte de este proceso, el reproductor podría cambiar el nombre del archivo.
7.  El reproductor copia el archivo original (sin convertir) en una carpeta de la jerarquía de carpetas music del usuario. Como parte de este proceso, el reproductor podría cambiar el nombre del archivo. Esta es la copia del archivo que usa el reproductor cuando el usuario sincroniza el contenido del equipo con un dispositivo que requiere el formato de archivo original. Este archivo se denomina archivo *de sombra.*
8.  El reproductor agrega información sobre el archivo convertido a la biblioteca. Esto incluye establecer el valor del atributo **ShadowFilePath** en la nueva ubicación donde se guarda el archivo de sombra.

Si necesita trabajar con el archivo convertido, puede consultar la biblioteca para recuperar el contenido mediante los atributos **ContentDistributor** y **WM/UniqueFileIdentifier.** Si necesita trabajar con el archivo de sombra, debe recuperar el objeto **Media** para el archivo convertido y, a continuación, consultar el **atributo ShadowFilePath.** Vea [Agregar metadatos a archivos convertidos.](adding-metadata-to-converted-files.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Acerca de los complementos de conversión**](about-conversion-plug-ins.md)
</dt> <dt>

[**Agregar metadatos a archivos convertidos**](adding-metadata-to-converted-files.md)
</dt> <dt>

[**Leer valores de atributo**](reading-attribute-values.md)
</dt> <dt>

[**Atributo ShadowFilePath**](shadowfilepath-attribute.md)
</dt> <dt>

[**Atributo WM/ContentDistributor**](wm-contentdistributor-attribute.md)
</dt> <dt>

[**Atributo WM/UniqueFileIdentifier**](wm-uniquefileidentifier-attribute.md)
</dt> </dl>

 

 




