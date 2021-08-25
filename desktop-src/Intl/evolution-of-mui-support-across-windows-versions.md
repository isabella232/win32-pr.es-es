---
description: Evolución de la compatibilidad con MUI en Windows versiones anteriores
ms.assetid: a3bda96e-6a54-41b3-88d3-9da88d7c0416
title: Evolución de la compatibilidad con MUI en Windows versiones anteriores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57e08ff181cf34daa95710d5bf57a294703a88ef
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122467902"
---
# <a name="evolution-of-mui-support-across-windows-versions"></a>Evolución de la compatibilidad con MUI en Windows versiones anteriores

-   [Antes de Windows Vista](#before-windows-vista)
-   [Windows Vista y más allá](#windows-vista-and-beyond)
    -   [Un sistema operativo neutral de lenguaje/MUI](#a-language-neutralmui-operating-system)
    -   [Los escenarios de implementación están totalmente basados en MUI](#deployment-scenarios-are-fully-mui-based)
    -   [Implementación de una sola imagen](#single-image-deployment)
    -   [Modelo de mantenimiento mejorado](#improved-servicing-model)
    -   [Infraestructura de TOI](#mui-infrastructure)
    -   [Administración de idiomas](#language-management)
    -   [Control de recursos](#resource-handling)

## <a name="before-windows-vista"></a>Antes de Windows Vista

Antes de la versión Windows Vista, Windows incluyeba imágenes de un solo idioma, lo que significaba que cada versión localizada de Windows contenía un único idioma para su interfaz de usuario. MUI era un complemento a la versión en inglés del sistema operativo y los paquetes de Interfaz de usuario multilingüe solo se podían agregar a determinadas versiones en inglés de Windows. Cuando se instala en la versión en inglés de Windows, LAI permite cambiar el idioma de la interfaz de usuario del sistema operativo según las preferencias de los usuarios individuales a uno de los idiomas admitidos.

El modelo del pack de MUI no exponía compatibilidad con MUI para las aplicaciones. Aunque los desarrolladores podían crear aplicaciones multilingües, tenían que crear sus propios mecanismos para hacerlo.

## <a name="windows-vista-and-beyond"></a>Windows Vista y más allá

Con Windows Vista, Microsoft realizó una inversión significativa en MUI. Windows Vista se ha creado desde el primer momento en una plataforma DE LAN. Aunque esto representa un avance importante en la estrategia de localización de Windows, ya que es un factor clave para que Microsoft proporcione Windows en más idiomas que nunca, es en primer lugar y ante todo un gran avance para los usuarios y clientes de Windows.

### <a name="a-language-neutralmui-operating-system"></a>Un sistema operativo neutral de lenguaje/MUI

La gran mayoría de Windows archivos binarios de Vista son compatibles con HIPAA y sus datos localizables se almacenan por separado del código. Esto ofrece flexibilidad, ya que se pueden agregar datos de lenguaje diferentes en cualquier momento.

### <a name="deployment-scenarios-are-fully-mui-based"></a>Los escenarios de implementación están totalmente basados en MUI

El diseño de instalación y empaquetado de Windows Vista se basa en MUI y todos los datos localizables se empaquetan en paquetes específicos del idioma, y cada paquete de idioma se puede implementar en distintos escenarios. Por ejemplo, aunque los DVD comerciales de Windows Vista contienen versiones de un solo idioma, los usuarios de ultimate edition pueden descargar paquetes de idioma adicionales de MUI y cambiar el idioma de la interfaz de usuario desde el panel de **control** Opciones regional e idioma. Enterprise licencias de edición obtienen todos los idiomas y pueden implementar cualquiera de ellos.

### <a name="single-image-deployment"></a>Implementación de una sola imagen

Enterprise clientes y OEM ahora pueden reducir el número de imágenes que necesitan mantener para implementar Windows y aplicaciones en equipos de diferentes configuraciones regionales a través de la implementación de una sola imagen.

Con MUI en Windows Vista, se puede implementar una imagen que contenga varios idiomas para cualquier usuario de idioma, y los usuarios pueden determinar sus propios idiomas preferidos (dentro de la directiva) durante la instalación o la "experiencia lista para usar" inicial con el equipo. En concreto, los OEM pueden colocar muchos idiomas de interfaz de usuario en sus equipos nuevos para permitir a los usuarios seleccionar uno de los Centro de bienvenida. Por lo tanto, a partir de una imagen con varios paquetes de idioma, el programa de instalación mostrará una lista de idiomas disponibles y permitirá a los usuarios elegir uno de ellos. A continuación, todas las configuraciones internacionales se establecen para que coincidan con el idioma o la configuración regional seleccionados.

### <a name="improved-servicing-model"></a>Modelo de mantenimiento mejorado

El mismo paquete de corrección de seguridad o QFE ahora se puede instalar sobre cualquier sistema de lenguaje. Esto es fundamental, ya que permite un cambio más rápido de las correcciones de seguridad en particular y permite que todos los usuarios internacionales se beneficien de la misma disponibilidad de tiempo de todas las correcciones de seguridad.

### <a name="mui-infrastructure"></a>Infraestructura de TOI

A partir de Windows Vista, las API de MUI están disponibles para permitir que los desarrolladores aprovechen los mecanismos de KPI para sus propias aplicaciones, sin tener que crear lógica personalizada para el control de recursos y la administración de lenguajes.

### <a name="language-management"></a>Administración de idiomas

Las API base de MUI que proporcionan funcionalidades de administración de lenguajes de interfaz de usuario están disponibles como parte de la infraestructura de MUI. Para ayudar a administrar las distintas configuraciones de idioma de la interfaz de usuario en el nivel de sistema, usuario y aplicación, ELI los combina internamente en una única lista con prioridad. DESPUÉS, LAN implementa un mecanismo de reserva basado en esta lista con prioridad, lo que permite soluciones de localización parciales y, al mismo tiempo, proporciona a los usuarios una experiencia de lenguaje de interfaz de usuario adecuada, si no la prefiere.

Por ejemplo, un sistema que ejecuta la versión en español de Windows Vista con un paquete de interfaz de idioma (LIP) de Español instalado sobre el sistema operativo base puede admitir el siguiente comportamiento: el sistema intentará y mostrará sus recursos en First EnRía y, si estos recursos no están disponibles en España, proporcione al usuario recursos españoles en su lugar.

### <a name="resource-handling"></a>Control de recursos

Gracias a la infraestructura de MUI mejorada que está disponible a partir de Windows Vista, la mayoría de las tecnologías de recursos comunes están habilitadas para MUI. En la tabla siguiente se proporcionan detalles adicionales sobre la compatibilidad con el control de recursos disponible en Windows Vista.




| Category | Soporte técnico | 
|----------|---------|
| Tipos de recurso admitidos | <ul><li>Recurso win32/no administrado: .DLL/.EXE/. OCX</li><li>Registros relacionados con shell</li><li>Recursos relacionados con la administración: registro de eventos, archivos snap-in/MSC</li><li>WMI: MOF/MFL</li><li>directiva de grupo: ADMX/ADML</li><li>Managed Resources.dll</li></ul> | 
| Herramientas de desarrollo | <ul><li>Para Win32: RC.exe, MUIRCT.exe y Visual Studio 2005 y versiones posteriores</li></ul> | 
| Compatibilidad limitada con tipos de recursos | <ul><li>*.chm archivos de ayuda</li></ul> | 




 

 

 



