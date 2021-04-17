---
description: Los servicios lingüísticos extendidos (ELS) se implementan como una biblioteca de vínculos dinámicos (DLL) que proporciona una gran variedad de funciones de compatibilidad lingüística para el texto que especifica la aplicación.
ms.assetid: 23d4e42a-a5bb-467c-a8b9-6a57ae39daa0
title: Acerca de los servicios lingüísticos extendidos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a6594fcfe67954a56cb09e239221b2b529d4d01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687835"
---
# <a name="about-extended-linguistic-services"></a>Acerca de los servicios lingüísticos extendidos

Los servicios lingüísticos extendidos (ELS) se implementan como una biblioteca de vínculos dinámicos (DLL) que proporciona una gran variedad de funciones de compatibilidad lingüística para el texto que especifica la aplicación. La tecnología incluye los complementos y la plataforma ELS para varios tipos de servicio lingüístico predefinidos a los que puede tener acceso la aplicación a través de la plataforma.

> [!Note]  
> El módulo ELS se instala automáticamente con Windows 7 y versiones posteriores.

 

## <a name="els-platform"></a>Plataforma ELS

La plataforma ELS es la interfaz entre la aplicación y los servicios de ELS. Proporciona una manera sencilla de implementar varios tipos de funcionalidad lingüística a través de la misma API, que permite a la aplicación tener acceso a servicios específicos y usarlos. Para obtener más información sobre la API, consulte [Extended lingüística Services Reference.](extended-linguistic-services-reference.md)

> [!Note]  
> Cuando la aplicación llama a cualquiera de las funciones de la API de ELS, la plataforma asigna memoria y recursos según sea necesario para la comunicación con los servicios. La aplicación es responsable de volver a llamar a la plataforma para liberar estos recursos.

 

La plataforma se ejecuta dentro del espacio de memoria virtual de la aplicación y toda la memoria asignada forma parte de este espacio. Por lo tanto, la aplicación solo necesita vincularse al archivo DLL del componente ELS (Elscore.dll) mediante la vinculación a Elscore. lib o mediante la carga dinámica de Elscore.dll.

## <a name="els-services"></a>Servicios ELS

En Windows 7 y versiones posteriores, la plataforma ELS solo admite los siguientes servicios predefinidos.

-   [Microsoft Detección de idioma](microsoft-language-detection.md)
-   [Detección de scripts de Microsoft](microsoft-script-detection.md)
-   [Servicios de transliteración](transliteration-services.md)

> [!Note]  
> Las versiones futuras de ELS serán compatibles con los servicios adicionales proporcionados por Microsoft o los proveedores de servicios.

 

Cada servicio está asociado a una categoría de servicio que describe lo que hace el servicio. La categoría se representa mediante una cadena no localizable. Lo usan las aplicaciones para enumerar los servicios disponibles. Las categorías de servicio actuales son:

-   "Detección de idioma"
-   "Detección de scripts"
-   Litera

La plataforma utiliza metadatos de servicio para enumerar los servicios solicitados por la aplicación. La aplicación puede usar las propiedades como el identificador único global (GUID) del servicio, los lenguajes y los scripts de entrada y salida admitidos, y la categoría de servicio para enumerar los servicios de ELS deseados.

Cada servicio ELS se implementa como un complemento compatible con un archivo DLL que se puede instalar en el sistema operativo para que la plataforma ELS pueda detectarlo y usarlo. Los servicios pueden exponer sus propios subservicios, si es necesario.

## <a name="main-els-operations"></a>Principales operaciones de ELS

En esta sección se describen las operaciones principales admitidas por la plataforma ELS. La plataforma admite modos de llamada sincrónicos y asincrónicos. El modo de llamada asincrónica utiliza un grupo de subprocesos de aplicación para programar subprocesos para el procesamiento de solicitudes.

> [!Note]  
> Dado que la plataforma admite un modo asincrónico, los servicios de ELS no tienen que implementar este tipo de funcionalidad por sí solos.

 

### <a name="service-enumeration"></a>Enumeración de servicios

La plataforma ELS carga y administra todos los servicios de ELS, lo que permite que la operación sea transparente para la aplicación. La aplicación enumera los servicios disponibles mediante una llamada a [**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices). Para obtener instrucciones de programación, consulte [enumeración y liberación de servicios](enumerating-and-freeing-services.md).

> [!Note]  
> Se recomienda por motivos de rendimiento que la aplicación Enumere los servicios disponibles una sola vez. La plataforma ELS comprueba los servicios de nuevo en la siguiente enumeración para asegurarse de que los resultados de la enumeración siempre están actualizados.

 

### <a name="text-recognition"></a>Reconocimiento de texto

Después de la enumeración de servicio, la aplicación llama a la función [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) para usar un servicio Els determinado para asignar cualquier intervalo de texto de texto de entrada al texto de salida. Un ejemplo de reconocimiento de texto es el uso de un servicio de detección de idiomas que recibe un segmento de texto y detecta su lenguaje más probable.

Una vez que el servicio reconoce el texto, [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) devuelve con una estructura de [**\_ \_ contenedor de propiedades de asignación**](/windows/desktop/api/Elscore/ns-elscore-mapping_property_bag) rellenada con los datos de salida y las propiedades generadas por el servicio. Para evitar pérdidas de memoria, la aplicación debe liberar el contenedor de propiedades mediante una llamada a [**MappingFreePropertyBag**](/windows/desktop/api/Elscore/nf-elscore-mappingfreepropertybag) para cada vez que [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) devuelva S \_ . Normalmente, la aplicación realiza esta acción cuando finaliza el uso de los datos de salida o cuando los datos de salida ya no son relevantes porque la región de entrada de texto se ha modificado, por ejemplo, editada o eliminada. Cuando se libera el contenedor de propiedades, **MappingFreePropertyBag** devuelve.

Se proporcionan instrucciones de programación para el reconocimiento de texto en la [solicitud de reconocimiento de texto](requesting-text-recognition.md).

### <a name="service-termination"></a>Terminación del servicio

Cuando la aplicación ya no necesita los servicios de ELS, llama a [**MappingFreeServices**](/windows/desktop/api/Elscore/nf-elscore-mappingfreeservices) antes de finalizar. Para obtener más información, consulte [enumeración y liberación de servicios](enumerating-and-freeing-services.md).

### <a name="versioning"></a>Control de versiones

Las versiones futuras de ELS permitirán la actualización de los servicios de ELS. La aplicación podrá comprobar los números de versión de la estructura de [**\_ \_ información del servicio de asignación**](/windows/desktop/api/Elscore/ns-elscore-mapping_service_info) para detectar los cambios en los servicios.

> [!Note]  
> La aplicación ELS no debe suponer que las distintas versiones del mismo servicio puedan recuperar exactamente los mismos resultados.

 

 

 



