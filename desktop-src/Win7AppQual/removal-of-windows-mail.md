---
description: Eliminación de Correo electrónico de Windows
ms.assetid: 356f0d79-12dd-49f0-b756-a46f20177efa
title: Eliminación de Correo electrónico de Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d50ad1008d9e252e1705a159f19d362677934023
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116283"
---
# <a name="removal-of-windows-mail"></a>Eliminación de Correo electrónico de Windows

## <a name="affected-platforms"></a>Plataformas afectadas

**Clientes:** Windows 7  
**Servidores:** Windows Server 2008 R2  









## <a name="feature-impact"></a>Impacto en las características

**Gravedad:** alta  
**Frecuencia:** alta  









## <a name="description"></a>Descripción

Microsoft está desusando la utilidad De Windows Mail y deshabilitando la API CoStartOutlookExpress. Las otras API de correo se han marcado como en desuso y están programadas para su eliminación en una versión posterior de Windows. Sin embargo, las API documentadas públicamente que no están marcadas como obsoletas o en desuso seguirán funcionando en Windows 7. Los archivos binarios permanecerán en los sistemas de los usuarios y seguirán siendo accesibles a través de las API, específicamente en los casos mencionados anteriormente. Además, los archivos de correo electrónico (.eml) y noticias (.nws) de los usuarios permanecerán en el sistema.

## <a name="manifestation-of-impact"></a>Demostración del impacto

La eliminación de Correo electrónico de Windows da como resultado lo siguiente:

-   Todos los puntos de entrada a Windows Mail y Contactos (por ejemplo, menú Inicio, accesos directos creados por el usuario, Iniciar -> Ejecutar, entre otros) se quitan o deshabilitan. Algunas de ellas se quitan por completo y otras producirán un error al intentar iniciarse.
-   Todos los archivos DLL se envían en el cuadro
-   Las API documentadas públicamente siguen funcionando como lo hacían en Windows Vista
-   Las API que intentan iniciar la interfaz de usuario principal del explorador se han modificado para crear un error silencioso. La función devolverá un resultado correcto, pero no mostrará la interfaz de usuario al usuario. Las API que llaman a otros cuadros de diálogo (por ejemplo, el administrador de trabajos de cola o el cuadro de diálogo Cuentas) siguen mostrando esa interfaz de usuario
-   Los controladores de protocolo (mailto, ldap, news, snews, nntp) no se asociarán con Windows Mail o Contacts. Al intentar iniciarlas, los clientes verán un cuadro de diálogo de error que les apunta a la ubicación donde pueden establecer estas asociaciones en otro programa.
-   Las asociaciones de archivo (.eml, .nws, .contact, .group, .wab, .p7c, .vfc) están rotas o deshabilitadas. Al intentar abrir un archivo con estas extensiones, los clientes recibirán un cuadro de diálogo que les ofrece otras aplicaciones instaladas que pueden usar y apuntarlas a una página web que ofrece soluciones.
-   Los archivos de usuario (por ejemplo, archivos de contacto o mensajes) permanecen en el sistema en el escenario de actualización
-   La carpeta Contactos está oculta de forma predeterminada para que los clientes no la vean.
-   Las API están marcadas como en desuso en MSDN
-   Se quita la función de vista previa del archivo
-   Se quitan los enlaces de shell en el menú contextual.
-   Se quita la función de búsqueda de archivos

## <a name="mitigation"></a>Mitigación

Los usuarios deben instalar Windows Live Mail o cualquier otro producto de correo que pueda leer archivos .eml y .nws.

## <a name="solution"></a>Solución

Detecte si hay un controlador de correo predeterminado instalado. Si no es así, informe al usuario de que instale Windows Live Mail o cualquier otro producto que pueda leer archivos .eml y .nws.

No diseñe código que llame a la API de interfaz de usuario de Windows Mail, ya que no funcionará. Debe encontrar otras maneras de acceder a los archivos .eml y .nws. Además, en cuanto sea factible, deje de depender de todas las demás API de Windows Mail.

## <a name="compatibility-performance-reliability-and-usability-testing"></a>Pruebas de compatibilidad, rendimiento, confiabilidad y facilidad de uso

-   Ejercicio de la aplicación en un entorno de Windows 7 para asegurarse de que la aplicación no intenta llamar a la API de interfaz de usuario.
-   Como alternativa, puede ejecutar Application Compatibility Toolkit (ACT) mediante el Evaluador de compatibilidad de Windows (WCE) para buscar posibles problemas debido al desuso de esta funcionalidad.

## <a name="links-to-other-resources"></a>Vínculos a otros recursos

<dl>

[Descarga del kit de herramientas de compatibilidad de aplicaciones](/windows-hardware/get-started/adk-install)  
</dl>

 

 
