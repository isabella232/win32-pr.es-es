---
description: PGM usa opciones de socket para establecer el estado, proporcionar parámetros de multidifusión e implementar sus funcionalidades de multidifusión.
ms.assetid: 91f5b051-cc42-46ba-88d9-680bd0367aff
title: Opciones de socket PGM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15e8df8050146774ac79d45594adcccf53a93d295ce42b9f00834aa0d699e83a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119860825"
---
# <a name="pgm-socket-options"></a>Opciones de socket PGM

PGM usa opciones de socket para establecer el estado, proporcionar parámetros de multidifusión e implementar sus funcionalidades de multidifusión. Esta página especifica cómo se deben establecer las opciones de socket PGM, enumera las opciones de socket disponibles para PGM y, si procede, proporciona ejemplos de uso e información adicional para varias opciones. Para obtener definiciones básicas de cada opción de socket PCM, vea [Opciones de socket](socket-options.md).

**Windows XP:** No se admite la programación de multidifusión confiable (PGM).

Las siguientes opciones de socket están disponibles para los remitentes PGM:

<dl> RM \_ LATEJOIN  
TAMAÑO DE \_ VENTANA \_ VELOCIDAD DE \_ RM  
VELOCIDAD \_ DE \_ ADV DE VENTANA DE ENVÍO DE \_ \_ RM  
ESTADÍSTICAS \_ DEL \_ REMITENTE DE RM  
MÉTODO RM \_ SENDER \_ WINDOW \_ \_ ADVANCE  
RM \_ SET \_ MCAST \_ TTL  
RM \_ SET \_ MESSAGE \_ BOUNDARY  
RM \_ SET \_ SEND \_ IF  
RM \_ USE \_ FEC  
</dl>

La opción RM SENDER WINDOW ADVANCE METHOD especifica el método utilizado al \_ avanzar la ventana de envío del borde \_ \_ \_ final. El parámetro optval solo puede ser E \_ WINDOW ADVANCE BY TIME \_ \_ \_ (valor predeterminado). Tenga en cuenta que no \_ se admite E WINDOW USE AS DATA \_ \_ \_ \_ CACHE.

Las siguientes opciones de socket están disponibles para los receptores PGM:

<dl> RM \_ ADD \_ RECEIVE \_ IF  
RM \_ DEL \_ RECEIVE \_ IF  
RM \_ HIGH \_ SPEED \_ INTRANET \_ OPT  
ESTADÍSTICAS \_ DEL \_ RECEPTOR DE RM  
</dl>

## <a name="setting-pgm-socket-options"></a>Establecer opciones de socket PGM

El fragmento de código siguiente muestra una guía de programación para establecer las opciones de socket PGM:


```C++

ULONG       OptionData;    // This structure is option-dependent
//     :
setsockopt (s,
            IPPROTO_RM,
            Socket_Option,
            (char *) &OptionData,
            sizeof (OptionData));


```



En el fragmento de código anterior, el tipo y el contenido de *OptionData* dependen de la opción de socket que se establezca. Para todas las opciones de socket PGM, el nivel de socket es IPPROTO \_ RM. Las opciones de socket PGM deben establecerse inmediatamente después de la llamada a la función [**bind,**](/windows/desktop/api/winsock/nf-winsock-bind) con las siguientes excepciones:

<dl> RM \_ SET \_ MESSAGE \_ BOUNDARY  
ESTADÍSTICAS \_ DEL \_ REMITENTE DE RM  
ESTADÍSTICAS \_ DEL \_ RECEPTOR DE RM  
</dl>

 

 



