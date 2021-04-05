---
title: Documentos y periféricos de documentos
description: Windows 7 proporciona a los desarrolladores una plataforma sólida para trabajar con documentos e integrar periféricos de documentos.
ms.assetid: 77d27775-eea8-4739-a1d2-05fcf6590cef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2e220949d37c17b95f92ed5026166ea71043354
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078155"
---
# <a name="documents-and-document-peripherals"></a>Documentos y periféricos de documentos

Windows 7 proporciona a los desarrolladores una plataforma sólida para trabajar con documentos e integrar periféricos de documentos. Se introdujeron dos nuevas tecnologías de documentos y almacenamiento en Windows Vista: XML Paper Specification (XPS) y Open Packaging Conventions (OPC). Estas tecnologías, que solo estaban disponibles en Windows Vista para los desarrolladores de aplicaciones de código administrado a través del marco de trabajo de Microsoft .NET, ahora están disponibles en el kit de desarrollo de Windows 7software (SDK) para su uso por parte de los desarrolladores de código no administrado.

## <a name="open-packaging-conventions"></a>Open Packaging Conventions

Windows 7 admite todos los formatos de archivo OPC, incluidos los de Microsoft, así como los de terceros. OPC es un componente de la especificación internacional de Office Open XML (OOXML) definida mediante *ISO/IEC DIS 29500* y *ECMA-376*. En función del formato de archivo *zip* , OPC permite a las aplicaciones almacenar una combinación de elementos de datos en un único archivo de paquete. Los desarrolladores de aplicaciones pueden usar las API de *empaquetado* de Windows 7 para crear, leer y manipular varios elementos de datos en archivos basados en OPC.

Con las API de *empaquetado* de Windows 7, los desarrolladores pueden crear nuevos formatos de paquete para adaptarse a los requisitos de almacenamiento de datos específicos de la aplicación.

Las firmas digitales de *X509* también son compatibles con las API de *empaquetado*. Los desarrolladores pueden usar las características de firma digital para firmar y validar las partes seleccionadas de un paquete OPC o todo el paquete. Las aplicaciones pueden proporcionar a sus documentos un nivel de seguridad adicional mediante el uso de firmas digitales para detectar cuándo se ha modificado el contenido de un archivo basado en OPC después de firmar el archivo. (Consulte [Introducción a las convenciones de empaquetado abierto](/previous-versions/windows/desktop/opc/open-packaging-conventions-overview)).

## <a name="xps-documents"></a>Documentos XPS

Los desarrolladores de aplicaciones de Windows pueden crear aplicaciones que generen documentos XPS con Windows 7. Esto les permite integrarse estrechamente con el ecosistema periférico del documento (dispositivos como escáneres e impresoras) y trabajar con documentos electrónicos seguros para admitir la publicación y el archivado.

En versiones anteriores de Windows, XPS no era compatible con los desarrolladores de Microsoft Win32. XPS se presentó en Windows Vista, pero la superficie de la API se limitó a los desarrolladores de .NET que trabajan con código administrado. Con Windows 7, los desarrolladores de Win32 pueden usar las nuevas API de *documento* XPS para reducir la cantidad de trabajo necesario para trabajar con XPS. Dado que XPS es la base de la nueva plataforma de impresión de Windows, esto supone una ventaja significativa.

En versiones anteriores de Windows, el acceso a la ruta de impresión XPS desde aplicaciones Win32 estaba limitado a los escapes de controlador. Esto redujo significativamente la utilidad de la ruta de impresión para que los desarrolladores no utilicen código administrado. Para los desarrolladores de Win32, la nueva API XPS *Print* reduce significativamente la cantidad de trabajo necesario para beneficiarse de las ventajas de la ruta de impresión XPS y elimina la necesidad de código de impresión en paralelo.

Los desarrolladores de aplicaciones pueden usar documentos XPS para compartir y archivar contenido como papel electrónico en formato de alta fidelidad, eficiente y confiable. Al igual que Windows Vista, la ruta de impresión en Windows 7 se basa en el formato XPS para proporcionar capacidades de impresión mejoradas. Las API de documentos XPS en Windows 7 proporcionan a los desarrolladores la capacidad de crear, tener acceso y manipular documentos XPS fácilmente. (Consulte la [Guía de programación de documentos XPS](/previous-versions//dd372978(v=vs.85))).

![visor de XPS](images/windows7-devguide-xpsviewer.jpg)

Los desarrolladores de aplicaciones de Windows pueden crear aplicaciones que generen documentos XPS con Windows 7

 

 