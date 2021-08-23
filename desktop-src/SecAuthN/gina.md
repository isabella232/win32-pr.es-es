---
description: El propósito de un archivo DLL de GINA es proporcionar procedimientos personalizables de identificación y autenticación de usuarios. Para ello, la GINA predeterminada delega la supervisión de eventos sas en Winlogon, que recibe y procesa las secuencias de atención seguras (SAS) CTL+ALT+DEL.
ms.assetid: 035e9c8b-2490-438d-8f02-7e0f039f960f
title: Gina
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5dad8917a24100fbf5c6c36eab3bbfc5b67baf62b378f9207626378fe864b672
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119623145"
---
# <a name="gina"></a>Gina

La [*GINA*](/windows/desktop/SecGloss/g-gly) funciona [](/windows/desktop/SecGloss/c-gly) en el contexto del proceso [*winlogon*](/windows/desktop/SecGloss/w-gly) y, como tal, el archivo DLL de GINA se carga muy pronto en el proceso de arranque. El archivo DLL de GINA debe seguir las reglas para que se mantenga la integridad del sistema, especialmente con respecto a la interacción con el usuario.

> [!Note]  
> Los archivos DLL de GINA se omiten Windows Vista.

 

El uso más común de la GINA es comunicarse con un dispositivo externo, como un lector de [*tarjetas inteligentes.*](/windows/desktop/SecGloss/r-gly) Es esencial establecer el parámetro start del controlador de dispositivo en el sistema (Winnt.h: SERVICE SYSTEM START) para asegurarse de que el controlador se carga en el momento en que se invoca \_ \_ el GINA.

El propósito de un archivo DLL de GINA es proporcionar procedimientos personalizables de identificación y autenticación de usuarios. Para ello, la GINA predeterminada delega la supervisión de eventos sas en Winlogon, que recibe y procesa las secuencias de atención [*seguras*](/windows/desktop/SecGloss/s-gly) (SAS) CTL+ALT+DEL. Una GINA personalizada es responsable de configurarse para recibir eventos SAS (distintos del evento DE SAS CTRL+ALT+SUPR predeterminado) y de notificar a Winlogon cuando se producen eventos sas. Winlogon evaluará su estado para determinar lo que se necesita para procesar la SAS de la GINA personalizada. Este procesamiento normalmente incluye llamadas a las funciones de procesamiento sas de GINA.

Para obtener información sobre funciones de exportación de GINA específicas, vea [Funciones de exportación de GINA](authentication-functions.md). Para obtener información sobre el uso de estructuras GINA para pasar información, vea [Estructuras de GINA.](authentication-structures.md)



| Tema                                                                             | Descripción                                                                     |
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [Carga y ejecución de un archivo DLL de GINA](loading-and-running-a-gina-dll.md)<br/>   | Qué valor de clave del Registro se va a modificar para cargar y ejecutar un archivo DLL de GINA personalizado.<br/> |
| [Compilar y probar un archivo DLL de GINA](building-and-testing-a-gina-dll.md)<br/> | Cómo probar un archivo DLL de GINA.<br/>                                              |



 

 

