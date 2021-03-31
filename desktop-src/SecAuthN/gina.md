---
description: El propósito de un archivo DLL de GINA es proporcionar procedimientos de autenticación e identificación de usuario personalizables. El GINA predeterminado lo hace mediante la delegación de la supervisión de eventos SAS en Winlogon, que recibe y procesa las secuencias de atención segura de CTL + ALT + Supr (SASs).
ms.assetid: 035e9c8b-2490-438d-8f02-7e0f039f960f
title: GINA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 084a65ad42bdbe030e697481501a4dc60e54baef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103816046"
---
# <a name="gina"></a>GINA

[*Gina*](/windows/desktop/SecGloss/g-gly) funciona en el [*contexto*](/windows/desktop/SecGloss/c-gly) del proceso [*Winlogon*](/windows/desktop/SecGloss/w-gly) y, como tal, el archivo dll de Gina se carga muy pronto en el proceso de arranque. El archivo DLL de GINA debe cumplir las reglas para que se mantenga la integridad del sistema, especialmente con respecto a la interacción con el usuario.

> [!Note]  
> Los archivos dll de GINA se omiten en Windows Vista.

 

El uso más común de GINA es comunicarse con un dispositivo externo como un [*lector*](/windows/desktop/SecGloss/r-gly)de tarjeta inteligente. Es esencial establecer el parámetro Start del controlador de dispositivo en System (Winnt. h: SERVICE \_ System \_ Start) para asegurarse de que el controlador se carga en el momento en que se invoca gina.

El propósito de un archivo DLL de GINA es proporcionar procedimientos de autenticación e identificación de usuario personalizables. El GINA predeterminado lo hace mediante la delegación de la supervisión de eventos SAS en Winlogon, que recibe y procesa las [*secuencias de atención segura*](/windows/desktop/SecGloss/s-gly) de CTL + Alt + Supr (Sass). Una GINA personalizada es responsable de configurarse para recibir eventos SAS (distintos del evento predeterminado CTRL + ALT + Supr) y notificar a Winlogon cuando se producen eventos SAS. Winlogon evaluará su estado para determinar lo que se necesita para procesar la SAS de GINA personalizada. Normalmente, este procesamiento incluye llamadas a las funciones de procesamiento de SAS de GINA.

Para obtener información sobre las funciones de exportación de GINA específicas, consulte [funciones de exportación de Gina](authentication-functions.md). Para obtener información sobre el uso de estructuras GINA para pasar información, consulte [estructuras Gina](authentication-structures.md).



| Tema                                                                             | Descripción                                                                     |
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [Cargar y ejecutar un archivo DLL de GINA](loading-and-running-a-gina-dll.md)<br/>   | El valor de clave del registro que se va a modificar para cargar y ejecutar un archivo DLL de GINA personalizado.<br/> |
| [Compilar y probar un archivo DLL de GINA](building-and-testing-a-gina-dll.md)<br/> | Cómo probar un archivo DLL de GINA.<br/>                                              |



 

 

