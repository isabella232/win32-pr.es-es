---
description: Al crear sus propios ensamblados en paralelo, siga las directrices para crear ensamblados en paralelo y crear cualquier DLL que se incluirá en el ensamblado de acuerdo con las instrucciones de creación de un archivo DLL para un ensamblado en paralelo.
ms.assetid: 0e98bbcd-7e23-4a33-b0fa-1f936d0ef96b
title: Crear almacenamiento de estado para ensamblados en paralelo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eee388cf680ee3a186a225ca7e3bde8b6eae625d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103814771"
---
# <a name="authoring-state-storage-for-side-by-side-assemblies"></a>Crear almacenamiento de estado para ensamblados en paralelo

Al crear sus propios ensamblados en paralelo, siga las [directrices para crear ensamblados en paralelo](guidelines-for-creating-side-by-side-assemblies.md) y crear cualquier dll que se incluirá en el ensamblado de acuerdo con las instrucciones de [creación de un archivo DLL para un ensamblado en paralelo](authoring-a-dll-for-a-side-by-side-assembly.md).

Siga las instrucciones siguientes para el almacenamiento del estado:

-   Almacenamiento del estado de diseño para que sea compatible con versiones anteriores y posteriores. Espere que las versiones se usen en cualquier orden: por ejemplo, V1, V3 y V2.
-   Inicialice y establezca la configuración predeterminada para el ensamblado en el código de ensamblado. No guarde los valores predeterminados en el registro.
-   La configuración del registro se debe escribir en una versión individual para aislar varias versiones de ensamblado que se pueden ejecutar al mismo tiempo. Diseñe el ensamblado en paralelo para almacenar y controlar correctamente el estado del ensamblado durante escenarios de uso compartido en paralelo.
-   Normalmente, los ensamblados almacenan información de estado en las claves del registro. Cree un conjunto de archivos de encabezado y funciones auxiliares para proporcionar una manera sencilla de crear una versión de las claves del registro que contenga el estado del ensamblado.
-   Cualquier información de estado de ensamblado guardada en el registro debe estar aislada de otras versiones del ensamblado. La configuración de estado almacenada en el registro se debe guardar en secciones de versión individuales del registro. Esto es necesario en las partes HKLM y HKCU del registro. Por ejemplo, almacene la configuración de estado de HKCU para la versión de ensamblado XXXX en la siguiente clave del registro:

    **HKCU** \\ **MyCompany** \\ **Componente** \\ **VersionXXXX**

-   Cualquier información de estado almacenada en el registro por ensamblados compartidos se debe guardar en secciones de versión individuales del registro. Por ejemplo, una configuración de estado denominada EnableSuperCoolFeature podría tener un valor **true** o **false**. Almacene el valor de un [*ensamblado en paralelo compartido*](s-sbscs-gly.md) como se indica a continuación:

    **HKEY \_ CurrentUser** \\ **software** \\ **MyCompany** \\  \\ **versión de 01.01** \\ **EnableSuperCoolFeature = true**

-   Cualquier información de estado almacenada en el registro por ensamblados privados debe guardarse en secciones de aplicación individuales del registro. Esto aísla la configuración de estado del ensamblado en la aplicación. Puede utilizar la función [**GetModuleFileName**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulefilenamea) para configurar una raíz virtual. Por ejemplo, si la versión de ensamblado XXYY es un ensamblado privado de "SomeApplication", una llamada a **GetModuleFileName** devuelve "SomeApplication" y cualquier configuración de estado privado para el ensamblado se debe escribir en la clave siguiente:

    **HKCU** \\ **MyCompany** \\ **Componente** \\ **VersionXXYY** \\ **SomeApplication**

-   Realice la configuración de estado compartido almacenada en el registro de forma privada en el contexto de ensamblado que ejecuta. Puede utilizar la función [**GetModuleFileName**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulefilenamea) para configurar una raíz virtual. Esto se debe hacer para las ramas HKLM y HKCU.
-   Idealmente, debe adoptar un modelo de persistencia en el que la aplicación conserve el estado y no modifique el registro. No es necesario que una aplicación toque directamente las entradas del registro del componente. En su lugar, el ensamblado debe ofrecer funciones de API que guardan o restauran configuraciones que son compatibles en paralelo.
-   Los ensamblados pueden guardar la configuración de estado en almacenes fuera del registro para permitir que el ensamblado interactúe con el estado global. Los ensamblados simultáneos pueden usar los siguientes almacenes compatibles en paralelo:
    -   Un almacén protegido (*pstore*)
    -   Una caché WinInet
    -   Un Microsoft SQL Server

 

 
