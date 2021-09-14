---
title: Documentos y periféricos de documentos
description: Windows 7 proporciona a los desarrolladores una plataforma sólida para trabajar con documentos e integrar periféricos de documentos.
ms.assetid: 77d27775-eea8-4739-a1d2-05fcf6590cef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2e220949d37c17b95f92ed5026166ea71043354
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359599"
---
# <a name="documents-and-document-peripherals"></a>Documentos y periféricos de documentos

Windows 7 proporciona a los desarrolladores una plataforma sólida para trabajar con documentos e integrar periféricos de documentos. Se han introducido dos nuevas tecnologías de almacenamiento y documentos en Windows Vista: XML Paper Specification (XPS) y Convenciones de empaquetado abierto (OPC). Estas tecnologías, que solo estaban disponibles en Windows Vista para desarrolladores de aplicaciones de código administrado a través de Microsoft .NET Framework, ahora están disponibles en el kit de desarrollo de software (SDK) de Windows 7 para que las usen los desarrolladores de código no administrado.

## <a name="open-packaging-conventions"></a>Open Packaging Conventions

Windows 7 admite todos los formatos de archivo OPC, incluidos los de Microsoft, así como los de terceros. OPC es un componente de la especificación internacional Office Open XML (OOXML) definida mediante *ISO/IEC DIS 29500* y *ECMA-376*. Según el formato *de archivo ZIP,* OPC permite a las aplicaciones almacenar una combinación de elementos de datos en un único archivo de paquete. Los desarrolladores de aplicaciones pueden usar las API de empaquetado de Windows 7 para crear, leer y manipular varios elementos de datos en archivos basados en OPC.

Con las *API de* empaquetado de Windows 7, los desarrolladores pueden crear nuevos formatos de paquete para adaptarse a los requisitos de almacenamiento de datos específicos de la aplicación.

Las firmas digitales *X509* también son compatibles con las *API de* empaquetado. Los desarrolladores pueden usar las características de firma digital para firmar y validar las partes seleccionadas de un paquete OPC o de todo el paquete. Las aplicaciones pueden proporcionar a sus documentos un nivel de seguridad adicional mediante el uso de firmas digitales para detectar cuándo se ha modificado el contenido de un archivo basado en OPC después de firmar el archivo. (Consulte [Convenciones de empaquetado abierto información general).](/previous-versions/windows/desktop/opc/open-packaging-conventions-overview)

## <a name="xps-documents"></a>Documentos XPS

Windows desarrolladores de aplicaciones pueden crear aplicaciones que generan documentos XPS con Windows 7. Esto les permite integrarse estrechamente con el ecosistema periférico de documentos (dispositivos como escáneres e impresoras) y trabajar con papel electrónico seguro para admitir la publicación y el archivado.

En versiones anteriores de Windows, XPS no era compatible con los desarrolladores de Microsoft Win32. XPS se introdujo en Windows Vista, pero la superficie de la API se limitaba a los desarrolladores de .NET que trabajan con código administrado. Con Windows 7, los desarrolladores de Win32 pueden usar las nuevas API de documentos *XPS* para reducir la cantidad de trabajo necesario al trabajar con XPS. Puesto que XPS es la base de la nueva Windows de impresión, eso es una ventaja importante.

En versiones anteriores de Windows, el acceso a la ruta de impresión XPS desde aplicaciones Win32 se limitaba a los escapes de controladores. Esto redujo significativamente la utilidad de la ruta de acceso de impresión para los desarrolladores que no usan código administrado. Para los desarrolladores de Win32, la nueva *API* de impresión XPS reduce significativamente la cantidad de trabajo necesario para beneficiarse de las ventajas de la ruta de impresión XPS y elimina la necesidad de código de impresión en paralelo.

Los desarrolladores de aplicaciones pueden usar documentos XPS para compartir y archivar contenido como papel electrónico en un formato de alta fidelidad, eficaz y de confianza. Al igual Windows Vista, la ruta de impresión de Windows 7 se basa en el formato XPS para proporcionar funcionalidades de impresión mejoradas. Las API de documentos XPS de Windows 7 permiten a los desarrolladores crear, acceder y manipular documentos XPS fácilmente. (Consulte [la Guía de programación de documentos XPS).](/previous-versions//dd372978(v=vs.85))

![xps viewer](images/windows7-devguide-xpsviewer.jpg)

Windows desarrolladores de aplicaciones pueden crear aplicaciones que generan documentos XPS con Windows 7

 

 