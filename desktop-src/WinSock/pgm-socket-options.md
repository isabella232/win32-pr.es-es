---
description: PGM usa opciones de socket para establecer el estado, proporcionar parámetros de multidifusión y, de lo contrario, implementar sus capacidades de multidifusión.
ms.assetid: 91f5b051-cc42-46ba-88d9-680bd0367aff
title: Opciones de socket PGM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5e2ec257043f86fabeafdc55ee0e7a828d495cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907938"
---
# <a name="pgm-socket-options"></a>Opciones de socket PGM

PGM usa opciones de socket para establecer el estado, proporcionar parámetros de multidifusión y, de lo contrario, implementar sus capacidades de multidifusión. En esta página se especifica cómo deben establecerse las opciones de socket PGM, se enumeran las opciones de socket disponibles para PGM y, si es necesario, se proporcionan ejemplos de uso e información adicional para diversas opciones. Para ver las definiciones básicas de cada opción de socket PCM, consulte [Opciones de socket](socket-options.md).

**Windows XP:** No se admite la programación multidifusión confiable (PGM).

Las siguientes opciones de socket están disponibles para los remitentes de PGM:

<dl> RM \_ LATEJOIN  
tamaño de la ventana de tasa de RM \_ \_ \_  
tasa de ADV. de \_ ventana de envío de RM \_ \_ \_  
Estadísticas del remitente de RM \_ \_  
\_ \_ \_ método avanzado de la ventana del remitente de RM \_  
RM \_ set \_ MCAST \_ TTL  
\_límite de \_ mensajes de conjunto de RM \_  
RM \_ establecer \_ envío \_ si  
RM \_ usar \_ FEC  
</dl>

La \_ opción método avanzado de la ventana del remitente de RM \_ \_ \_ especifica el método que se usa al avanzar la ventana de envío del borde final. El parámetro optval solo puede ser la \_ ventana E \_ avanzar \_ por \_ tiempo (el valor predeterminado). Tenga en cuenta \_ que \_ \_ no se admite la utilización de la ventana en la \_ \_ memoria caché de datos.

Las siguientes opciones de socket están disponibles para los receptores de PGM:

<dl> \_Agregar recepción de RM \_ \_ si  
RM \_ del \_ receptor \_ si  
RM de \_ alta velocidad de la \_ \_ intranet \_ OPC  
\_estadísticas del receptor de RM \_  
</dl>

## <a name="setting-pgm-socket-options"></a>Configuración de las opciones de socket PGM

En el fragmento de código siguiente se muestra una directriz de programación para establecer las opciones de socket PGM:


```C++

ULONG       OptionData;    // This structure is option-dependent
//     :
setsockopt (s,
            IPPROTO_RM,
            Socket_Option,
            (char *) &OptionData,
            sizeof (OptionData));


```



En el fragmento de código anterior, el tipo y el contenido de *OptionData* dependen de la opción de socket que se establece. Para todas las opciones de socket PGM, el nivel de socket es IPPROTO \_ RM. Las opciones de socket PGM se deben establecer inmediatamente después de la llamada a la función de [**enlace**](/windows/desktop/api/winsock/nf-winsock-bind) , con las siguientes excepciones:

<dl> \_límite de \_ mensajes de conjunto de RM \_  
Estadísticas del remitente de RM \_ \_  
\_estadísticas del receptor de RM \_  
</dl>

 

 



