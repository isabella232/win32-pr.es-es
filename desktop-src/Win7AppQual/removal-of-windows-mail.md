---
description: .
ms.assetid: 356f0d79-12dd-49f0-b756-a46f20177efa
title: Eliminación de Windows Mail
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 836b2f447735c8e3595955ca7e99f1ae818c3d5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278787"
---
# <a name="removal-of-windows-mail"></a>Eliminación de Windows Mail

## <a name="affected-platforms"></a>Plataformas afectadas

**Clientes** : Windows 7  
**Servidores** : Windows Server 2008 R2  









## <a name="feature-impact"></a>Impacto en las características

**Gravedad** alta  
**Frecuencia** : alta  









## <a name="description"></a>Descripción

Microsoft está dejando de usar la utilidad Windows Mail y deshabilitando la API CoStartOutlookExpress. Las otras API de correo se han marcado como desusadas y están preparadas para su eliminación en una versión posterior de Windows. Sin embargo, las API documentadas públicamente que no estén marcadas como desusadas u obsoletas seguirán funcionando en Windows 7. Los archivos binarios permanecerán en los sistemas de los usuarios y seguirán siendo accesibles a través de las API, específicamente en los casos mencionados anteriormente. Además, los archivos de correo electrónico (. eml) y News (. NWS) de los usuarios permanecerán en el sistema.

## <a name="manifestation-of-impact"></a>Manifiesto de impacto

La eliminación de Windows Mail da como resultado lo siguiente:

-   Todos los puntos de entrada a correo y contactos de Windows (por ejemplo, menú Inicio, accesos directos creados por el usuario, Inicio > ejecución, etc.) se quitan o deshabilitan. Algunos de ellos se quitan por completo, se producirá un error en otros al intentar iniciar.
-   Todos los archivos DLL se incluyen en el cuadro
-   Las API documentadas públicamente continúan funcionando como en Windows Vista
-   Todas las API que intenten iniciar la interfaz de usuario principal del explorador se han modificado para crear un error silencioso. La función devolverá un valor correcto, pero no mostrará la interfaz de usuario al usuario. Las API que llaman a otros cuadros de diálogo (por ejemplo, el administrador de trabajos de impresión o el cuadro de diálogo cuentas) siguen mostrando esa interfaz de usuario
-   Los controladores de protocolo (mailto, LDAP, News, SNEWS, NNTP) no se asociarán a Windows Mail ni a los contactos. Al intentar iniciarlos, los clientes verán un cuadro de diálogo de error que apuntan a la ubicación en la que pueden establecer estas asociaciones en otro programa.
-   Las asociaciones de archivo (. eml,. NWS,. contact,. Group,. WAB,. p7c,. VFC) están dañadas o deshabilitadas. Al intentar abrir un archivo con estas extensiones, los clientes recibirán un cuadro de diálogo que les ofrece otras aplicaciones que se instalan y que pueden apuntar a una página web que ofrece soluciones.
-   Los archivos de usuario (por ejemplo, los archivos o mensajes de contacto) permanecen en el sistema en el escenario de actualización
-   La carpeta contactos está oculta de forma predeterminada para que los clientes no la vean
-   Las API se marcan como desusadas en MSDN
-   Se ha quitado la función de vista previa de archivo
-   Se quitan los enlaces de Shell en el menú contextual
-   Se quita la función de búsqueda de archivos

## <a name="mitigation"></a>Mitigación

Los usuarios deben instalar Windows Live Mail o cualquier otro producto de correo que pueda leer archivos. eml y. nws.

## <a name="solution"></a>Solución

Detecta si hay un controlador de correo predeterminado instalado. Si no es así, aconseje a los usuarios que instalen Windows Live Mail o cualquier otro producto que pueda leer archivos. eml y. nws.

No diseñe código que llame a la API de la interfaz de usuario de Windows Mail, ya que no funcionará. Debe encontrar otras maneras de acceder a los archivos. eml y. nws. Además, en cuanto sea factible, descontinúe su dependencia en todas las demás API de Windows Mail.

## <a name="compatibility-performance-reliability-and-usability-testing"></a>Pruebas de compatibilidad, rendimiento, confiabilidad y facilidad de uso

-   Ejecute la aplicación en un entorno de Windows 7 para asegurarse de que la aplicación no intente llamar a la API de la interfaz de usuario.
-   Como alternativa, puede ejecutar el kit de herramientas de compatibilidad de aplicaciones (ACT) mediante el evaluador de compatibilidad de Windows (WCE) para localizar cualquier posible problema debido al desuso de esta funcionalidad.

## <a name="links-to-other-resources"></a>Vínculos a otros recursos

<dl>

[Descarga del kit de herramientas de compatibilidad de aplicaciones](/windows-hardware/get-started/adk-install)  
</dl>

 

 
