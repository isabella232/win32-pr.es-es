---
title: Configuración de la aplicación
description: La instalación de una aplicación para un solo usuario puede crear problemas en un entorno multiusuario Servicios de Escritorio remoto usuario.
ms.assetid: 3e60e95a-3580-48aa-a9f9-8fd899aa7fca
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58f3c53f2370f4123352489ac747546e3335c558
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127249969"
---
# <a name="application-setup"></a>Configuración de la aplicación

El procedimiento de instalación automatizada para muchas aplicaciones existentes supone que la aplicación se está instalando para un solo usuario. En un entorno multiusuario Servicios de Escritorio remoto, esta suposición puede crear los siguientes problemas:

-   Si el procedimiento de instalación actualiza el registro y el entorno de escritorio para un solo usuario, los usuarios adicionales deben volver a instalar todo el paquete o un administrador debe copiar manualmente la información del registro y el escritorio de un usuario a los demás usuarios.
-   Con algunos procedimientos de instalación, puede personalizar la aplicación en el momento de la instalación mediante la exclusión de características. Si el instalador inicial excluye parte de la aplicación, los usuarios adicionales deben volver a instalar la aplicación para obtener las características excluidas.

Para evitar estos problemas, los procedimientos de instalación deben usar las siguientes directrices al instalar una aplicación en un servidor de host de sesión de Escritorio remoto (host de sesión de Escritorio remoto):

-   Instale las aplicaciones en el entorno de usuario predeterminado común a todos los usuarios. Antes de instalar la aplicación, ejecute el comando **change user /install** console y, una vez completada la instalación, ejecute el comando **change user /execute** console. Use un Servicios de Escritorio remoto de compatibilidad para la instalación.
-   Admitir la personalización específica del usuario mediante el uso de perfiles de usuario. Para ello, cree un formato de archivo de [plantilla administrativa](/previous-versions/windows/desktop/Policy/administrative-template-file-format) para que un administrador pueda configurar el Registro para indicar las características disponibles para cada usuario. A continuación, en tiempo de ejecución, la aplicación puede habilitar o deshabilitar características en función de la configuración del Registro del usuario actual. La aplicación puede almacenar la configuración por usuario en el subárbol del Registro **HKEY CURRENT USER** y permitir que cada usuario configure la aplicación según sus preferencias.

 

 