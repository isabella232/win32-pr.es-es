---
description: Administrar el uso compartido de ensamblados y el control de versiones de DLL en el almacén de ensamblados en paralelo de los sistemas desde programas. Escriba manifiestos de ensamblado y describa automáticamente las aplicaciones para compartir ensamblados y redirigir archivos DLL.
ms.assetid: 2f841eb6-9a6c-4c9b-b057-a3da6cd6b0b0
title: Aplicaciones aisladas y ensamblados en paralelo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59abfbd5392040856c66ef9eb786b66d2a84500f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127271516"
---
# <a name="isolated-applications-and-side-by-side-assemblies"></a>Aplicaciones aisladas y ensamblados en paralelo

## <a name="purpose"></a>Propósito

Aplicaciones aisladas y ensamblados en paralelo es una solución de Microsoft Windows que reduce los conflictos de control de versiones en Windows aplicaciones cliente. Con Windows, los desarrolladores de aplicaciones pueden compilar aplicaciones aisladas que son totalmente autodescriptas y no se ven afectadas por cambios en el Registro, otras aplicaciones u otras versiones de ensamblados que se ejecutan en el sistema. Los autores y administradores de aplicaciones pueden usar manifiestos para administrar el uso compartido de ensamblados en paralelo después de la implementación de forma global o por aplicación. Los clientes se benefician de las aplicaciones aisladas que son más estables y se actualizan de forma más confiable.

## <a name="where-applicable"></a>Donde sea aplicable

Las aplicaciones aisladas y el uso compartido de ensamblados en paralelo se pueden usar para desarrollar aplicaciones que compartan de forma segura ensamblados de sistema operativo. Los desarrolladores pueden usar esta tecnología para corregir los conflictos de control de versiones de DLL causados por una versión incompatible de un ensamblado compartido.

Si la aplicación debe obtener de forma coherente la versión de un componente que ha probado, es posible aislar la aplicación para que siempre se ejecute con la versión probada del componente en el equipo del usuario.

Las aplicaciones aisladas y los ensamblados en paralelo están diseñados para el desarrollo de aplicaciones de estilo de escritorio.

## <a name="developer-audience"></a>Audiencia de desarrolladores

Esta documentación está pensada principalmente para desarrolladores de software, desarrolladores de aplicaciones y administradores de red:

-   Desarrolladores de software que desean crear aplicaciones aisladas que usarán los ensamblados en paralelo que Microsoft y otros publicadores de ensamblados en paralelo han puesto a disposición de los usuarios.
-   Desarrolladores de aplicaciones que están interesados en crear sus propios ensamblados en paralelo para aislar sus aplicaciones.
-   Administradores de red que desean más información sobre las aplicaciones aisladas.

Como referencia principal para el uso compartido de ensamblados en paralelo y las aplicaciones aisladas, esta documentación proporciona información general sobre la creación de manifiestos y ensamblados en paralelo, la instalación de aplicaciones aisladas y ensamblados en paralelo y el uso de activation Context API.

## <a name="run-time-requirements"></a>Requisitos de tiempo de ejecución

Windows Server 2003 y versiones posteriores o Windows XP y versiones posteriores son necesarios para usar ensamblados y manifiestos en paralelo para aislar aplicaciones y usar activation Context API.

## <a name="in-this-section"></a>En esta sección



| Tema                                                         | Descripción                                                                    |
|---------------------------------------------------------------|--------------------------------------------------------------------------------|
| [Referencia](side-by-side-assemblies-reference.md)<br/> | Documentación de aplicaciones aisladas y ensamblados en paralelo.<br/> |



 

 

 




