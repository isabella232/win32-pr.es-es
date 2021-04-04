---
title: Acerca del proceso de conversión
description: Acerca del proceso de conversión
ms.assetid: 147b82fd-9e82-4acf-8f8a-43eb02e99024
keywords:
- Windows Media Player, proceso de conversión
- Complementos de Windows Media Player, conversión
- complementos, conversión
- Complementos de conversión, proceso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d6fe2f2bbedf03b78c0d19abaf3793e8e92c788
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104077333"
---
# <a name="about-the-conversion-process"></a>Acerca del proceso de conversión

Una vez que Windows Media Player crea una instancia del complemento de conversión, el proceso continúa como sigue:

1.  El reproductor llama a [IWMPConvert:: ConvertFile](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpconvert-convertfile).
2.  El complemento convierte el archivo proporcionado en el parámetro *bstrInputFile* en un formato ASF.
3.  Si por algún motivo se produce un error en la conversión, el complemento devuelve un código de error adecuado y el proceso se detiene.
4.  Si la conversión se realiza correctamente, el complemento coloca el archivo convertido en la carpeta proporcionada en el parámetro *bstrDestinationFolder* y devuelve la ruta de acceso completa al archivo convertido mediante el parámetro *pbstrOutputFile* .
5.  El complemento devuelve un código de éxito de **ConvertFile**.
6.  El reproductor copia el archivo convertido en una carpeta de la jerarquía de carpetas de música del usuario. Exactamente donde el reproductor copia el archivo en depende del contenido. Como parte de este proceso, el reproductor podría cambiar el nombre del archivo.
7.  El reproductor copia el archivo original (desconvertido) en una carpeta de la jerarquía de carpetas de música del usuario. Como parte de este proceso, el reproductor podría cambiar el nombre del archivo. Esta es la copia del archivo que usa el reproductor cuando el usuario sincroniza el contenido del equipo con un dispositivo que requiere el formato de archivo original. Este archivo se denomina *archivo de instantáneas*.
8.  El reproductor agrega información sobre el archivo convertido a la biblioteca. Esto incluye establecer el valor del atributo **ShadowFilePath** en la nueva ubicación donde se guarda el archivo de instantáneas.

Si necesita trabajar con el archivo convertido, puede consultar la biblioteca para recuperar el contenido mediante los atributos **ContentDistributor** y **WM/UniqueFileIdentifier** . Si necesita trabajar con el archivo de instantáneas, debe recuperar el objeto **multimedia** del archivo convertido y, a continuación, consultar el atributo **ShadowFilePath** . Vea [Agregar metadatos a archivos convertidos](adding-metadata-to-converted-files.md).

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

 

 




