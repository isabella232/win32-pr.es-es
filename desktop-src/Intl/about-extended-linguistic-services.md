---
description: Extended Linguistic Services (ELS) se implementa como una biblioteca de vínculos dinámicos (DLL) que proporciona una variedad de funcionalidades de compatibilidad lingüística para el texto que especifica la aplicación.
ms.assetid: 23d4e42a-a5bb-467c-a8b9-6a57ae39daa0
title: Acerca de los servicios lingüísticos extendidos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a6594fcfe67954a56cb09e239221b2b529d4d01
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127274892"
---
# <a name="about-extended-linguistic-services"></a>Acerca de los servicios lingüísticos extendidos

Extended Linguistic Services (ELS) se implementa como una biblioteca de vínculos dinámicos (DLL) que proporciona una variedad de funcionalidades de compatibilidad lingüística para el texto que especifica la aplicación. La tecnología incluye la plataforma ELS y complementos para varios tipos de servicios lingüísticos predefinidos accesibles para la aplicación a través de la plataforma.

> [!Note]  
> El módulo ELS se instala automáticamente con Windows 7 y versiones posteriores.

 

## <a name="els-platform"></a>Plataforma ELS

La plataforma ELS es la interfaz entre la aplicación y los servicios de ELS. Proporciona una manera sencilla de implementar varios tipos de funcionalidad lingüística a través de la misma API, lo que permite a la aplicación acceder a servicios específicos y usarlos. Para obtener más información sobre la API, vea [Referencia de Servicios lingüísticos extendidos.](extended-linguistic-services-reference.md)

> [!Note]  
> Cuando la aplicación llama a cualquiera de las funciones de LA API de ELS, la plataforma asigna memoria y recursos según sea necesario para la comunicación con los servicios. La aplicación es responsable de llamar de nuevo a la plataforma para liberar estos recursos.

 

La plataforma se ejecuta dentro del espacio de memoria virtual de la aplicación y toda la memoria asignada forma parte de este espacio. Por lo tanto, la aplicación solo necesita vincular a la DLL del componente ELS (Elscore.dll) mediante la vinculación a Elscore.lib o mediante la carga dinámica de Elscore.dll.

## <a name="els-services"></a>Servicios DE ELS

Para Windows 7 y versiones posteriores, la plataforma ELS solo admite los siguientes servicios predefinidos.

-   [Microsoft Detección de idioma](microsoft-language-detection.md)
-   [Detección de scripts de Microsoft](microsoft-script-detection.md)
-   [Servicios de transliteración](transliteration-services.md)

> [!Note]  
> Las versiones futuras de ELS admitirán servicios adicionales proporcionados por Microsoft o proveedores de servicios.

 

Cada servicio está asociado a una categoría de servicio que describe lo que hace el servicio. La categoría se representa mediante una cadena no localizable. Las aplicaciones lo usan para enumerar los servicios disponibles. Las categorías de servicio actuales son:

-   "Detección de idioma"
-   "Detección de scripts"
-   "Transliteración"

La plataforma usa metadatos de servicio para enumerar los servicios solicitados por la aplicación. La aplicación puede usar propiedades como el identificador único global (GUID) del servicio, los scripts y los lenguajes de entrada y salida admitidos y la categoría de servicio para enumerar los servicios ELS deseados.

Cada servicio ELS se implementa como un complemento compatible con un archivo DLL que se puede instalar en el sistema operativo para que la plataforma elS pueda detectarlo y usarlo. Los servicios pueden exponer sus propios subservicios, si es necesario.

## <a name="main-els-operations"></a>Operaciones principales de ELS

En esta sección se describen las operaciones principales admitidas por la plataforma ELS. La plataforma admite modos de llamada sincrónicos y asincrónicos. El modo de llamada asincrónica usa un grupo de subprocesos de aplicación para programar subprocesos para procesar solicitudes.

> [!Note]  
> Puesto que la plataforma admite un modo asincrónico, los servicios elS no tienen que implementar este tipo de funcionalidad por sí mismos.

 

### <a name="service-enumeration"></a>Enumeración de servicios

La plataforma ELS carga y administra todos los servicios de ELS, lo que hace que la operación sea transparente para la aplicación. La aplicación enumera los servicios disponibles llamando a [**MappingGetServices.**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices) Para obtener instrucciones de programación, [vea Enumerating and Freeing Services](enumerating-and-freeing-services.md).

> [!Note]  
> Por motivos de rendimiento, es aconsejable que la aplicación enumere los servicios disponibles una sola vez. La plataforma ELS vuelve a comprobar los servicios en la enumeración siguiente para asegurarse de que sus resultados de enumeración siempre están actuales.

 

### <a name="text-recognition"></a>Reconocimiento de texto

Después de la enumeración del servicio, la aplicación llama a la función [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) para usar un servicio ELS determinado para asignar cualquier intervalo de texto de texto de entrada al texto de salida. Un ejemplo de reconocimiento de texto es el uso de un servicio de detección de idioma que recibe un segmento de texto y detecta su idioma más probable.

Una vez que el servicio ha reconocido el texto, [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) devuelve con una estructura [**MAPPING PROPERTY \_ \_ BAG**](/windows/desktop/api/Elscore/ns-elscore-mapping_property_bag) rellenada con los datos de salida y las propiedades producidas por el servicio. Para evitar pérdidas de memoria, la aplicación debe liberar el bolsa de propiedades llamando a [**MappingFreePropertyBag**](/windows/desktop/api/Elscore/nf-elscore-mappingfreepropertybag) cada vez que [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) devuelva S \_ OK. Normalmente, la aplicación hace esto cuando termina de usar los datos de salida o cuando los datos de salida ya no son pertinentes porque la región de entrada de texto se ha modificado, por ejemplo, editado o eliminado. Cuando se libera el bolsa de propiedades, **mappingFreePropertyBag devuelve** .

Las instrucciones de programación para el reconocimiento de texto se [proporcionan en Solicitud de reconocimiento de texto](requesting-text-recognition.md).

### <a name="service-termination"></a>Finalización del servicio

Cuando la aplicación ya no requiere servicios ELS, llama a [**MappingFreeServices**](/windows/desktop/api/Elscore/nf-elscore-mappingfreeservices) antes de finalizar. Para obtener más información, [vea Enumerating and Freeing Services](enumerating-and-freeing-services.md).

### <a name="versioning"></a>Control de versiones

Las versiones futuras de ELS permitirán actualizar los servicios de ELS. La aplicación podrá comprobar los números de versión de la estructura [**DE INFORMACIÓN DE MAPPING \_ SERVICE \_**](/windows/desktop/api/Elscore/ns-elscore-mapping_service_info) para detectar cualquier cambio en los servicios.

> [!Note]  
> La aplicación ELS no debe suponer que las distintas versiones del mismo servicio pueden recuperar exactamente los mismos resultados.

 

 

 



