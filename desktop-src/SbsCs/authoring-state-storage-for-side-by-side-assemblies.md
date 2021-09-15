---
description: Al crear sus propios ensamblados en paralelo, siga las instrucciones para crear ensamblados en paralelo y cree cualquier archivo DLL que se incluya en el ensamblado según las directrices de Creación de un archivo DLL para un ensamblado en paralelo.
ms.assetid: 0e98bbcd-7e23-4a33-b0fa-1f936d0ef96b
title: Estado de Storage para ensamblados en paralelo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eee388cf680ee3a186a225ca7e3bde8b6eae625d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127271703"
---
# <a name="authoring-state-storage-for-side-by-side-assemblies"></a>Estado de Storage para ensamblados en paralelo

Al crear sus propios ensamblados en paralelo, siga las instrucciones para crear ensamblados en paralelo y cree cualquier archivo DLL que se incluya en el ensamblado según las [directrices](guidelines-for-creating-side-by-side-assemblies.md) de Creación de un archivo [DLL](authoring-a-dll-for-a-side-by-side-assembly.md)para un ensamblado en paralelo.

Siga las siguientes directrices para el almacenamiento del estado:

-   Diseñe el almacenamiento de estado para que sea compatible con versiones anteriores y hacia delante. Espere que las versiones se usen en cualquier orden: por ejemplo, v1, v3 y v2.
-   Inicialice y establezca la configuración predeterminada del ensamblado en el código del ensamblado. No guarde la configuración predeterminada en el Registro.
-   La configuración del Registro debe escribirse en una versión individual para aislar varias versiones de ensamblado que se pueden ejecutar al mismo tiempo. Diseñe el ensamblado en paralelo para almacenar y controlar correctamente el estado del ensamblado durante los escenarios de uso compartido en paralelo.
-   Normalmente, los ensamblados almacenan información de estado en las claves del Registro. Cree un conjunto de archivos de encabezado y funciones auxiliares para proporcionar una manera sencilla de crear versiones de las claves del Registro que contienen el estado del ensamblado.
-   Cualquier información de estado de ensamblado guardada en el Registro debe aislarse de otras versiones del ensamblado. La configuración de estado almacenada en el registro debe guardarse en secciones de versión individuales del registro. Esto es necesario en las partes HKLM y HKCU del registro. Por ejemplo, almacene la configuración de estado HKCU para la versión del ensamblado XXXX en la siguiente clave del Registro:

    **HKCU** \\ **MyCompany** \\ **MyComponent** \\ **VersionXXXX**

-   Cualquier información de estado almacenada en el Registro por ensamblados compartidos debe guardarse en secciones de versión individuales del registro. Por ejemplo, una configuración de estado denominada EnableSuper CoolFeature podría tener un valor **de TRUE** o **FALSE.** Almacene el valor de un [*ensamblado compartido en paralelo*](s-sbscs-gly.md) como se muestra a continuación:

    **HKEY \_ CurrentUser** \\ **Software** \\ **MyCompany** \\ **MyComponent** \\ **Version01.01** \\ **EnableSuper CoolFeature = TRUE**

-   Cualquier información de estado almacenada en el Registro por ensamblados privados debe guardarse en secciones de aplicación individuales del registro. Esto aísla la configuración de estado del ensamblado en la aplicación. Puede usar la [**función GetModuleFileName**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulefilenamea) para configurar una raíz virtual. Por ejemplo, si la versión del ensamblado XXYY es un ensamblado privado de "SomeApplication", una llamada a **GetModuleFileName** devuelve "SomeApplication" y cualquier configuración de estado privado para el ensamblado debe escribirse con la clave siguiente:

    **HKCU** \\ **MyCompany** \\ **MyComponent** \\ **VersionXXYY** \\ **SomeApplication**

-   Haga que la configuración de estado compartido almacenada en el Registro sea privada para el contexto de ensamblado que se ejecuta. Puede usar la [**función GetModuleFileName**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulefilenamea) para configurar una raíz virtual. Esto debe hacerse para las ramas HKLM y HKCU.
-   Lo ideal es adoptar un modelo de persistencia en el que la aplicación conserve el estado y no modifique el registro. Una aplicación no debe tener que tocar directamente las entradas del Registro del componente. En su lugar, el ensamblado debe ofrecer funciones de API que guarden o restauren la configuración que sea compatible en paralelo.
-   Los ensamblados pueden guardar la configuración de estado en almacenes fuera del Registro para permitir que el ensamblado interactúe con el estado global. Los ensamblados en paralelo pueden usar los siguientes almacenes compatibles en paralelo:
    -   Un almacén protegido (*pstore*)
    -   Una caché de WinInet
    -   Un Microsoft SQL Server

 

 
