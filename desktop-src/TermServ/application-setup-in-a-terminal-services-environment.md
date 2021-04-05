---
title: Configuración de la aplicación
description: La instalación de una aplicación para un solo usuario puede crear problemas en un entorno de Servicios de Escritorio remoto multiusuario.
ms.assetid: 3e60e95a-3580-48aa-a9f9-8fd899aa7fca
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58f3c53f2370f4123352489ac747546e3335c558
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359275"
---
# <a name="application-setup"></a>Configuración de la aplicación

El procedimiento de instalación automatizada para muchas aplicaciones existentes supone que la aplicación se está instalando para un solo usuario. En un entorno de Servicios de Escritorio remoto multiusuario, esta suposición puede crear los siguientes problemas:

-   Si el procedimiento de instalación actualiza el entorno de escritorio y del registro para un solo usuario, los usuarios adicionales deben volver a instalar el paquete completo, o bien un administrador debe copiar manualmente la información del registro y del escritorio de un usuario a los demás usuarios.
-   Con algunos procedimientos de instalación, puede personalizar la aplicación en el momento de la instalación excluyendo las características. Si el instalador inicial excluye parte de la aplicación, los usuarios adicionales deben volver a instalar la aplicación para obtener las características excluidas.

Para evitar estos problemas, los procedimientos de configuración deben usar las siguientes directrices al instalar una aplicación en un servidor host de sesión de Escritorio remoto (host de sesión de escritorio remoto):

-   Instalar las aplicaciones en el entorno de usuario predeterminado común a todos los usuarios. Antes de instalar la aplicación, ejecute el comando **Change User/Install** Console y, una vez completada la instalación, ejecute el comando **Change User/Execute** Console. Use un script de compatibilidad de Servicios de Escritorio remoto para la instalación.
-   Admita la personalización específica del usuario mediante el uso de perfiles de usuario. Para ello, cree un [formato de archivo de plantilla administrativa](/previous-versions/windows/desktop/Policy/administrative-template-file-format) para que un administrador pueda configurar el registro para indicar las características disponibles para cada usuario. A continuación, en tiempo de ejecución, la aplicación puede habilitar o deshabilitar características en función de la configuración de la configuración del registro del usuario actual. La aplicación puede almacenar la configuración por usuario en el subárbol del registro de **usuario actual de HKEY** y permitir que todos los usuarios configuren la aplicación según sus preferencias.

 

 