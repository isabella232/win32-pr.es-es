---
description: Administrar el uso compartido de ensamblados y el control de versiones de DLL en el almacén de ensamblados en paralelo de los sistemas desde programas. Escriba manifiestos de ensamblado y aplicaciones autodescriptivas para el uso compartido de ensamblados y redirección de dll.
ms.assetid: 2f841eb6-9a6c-4c9b-b057-a3da6cd6b0b0
title: Aplicaciones aisladas y ensamblados en paralelo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59abfbd5392040856c66ef9eb786b66d2a84500f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154098"
---
# <a name="isolated-applications-and-side-by-side-assemblies"></a>Aplicaciones aisladas y ensamblados en paralelo

## <a name="purpose"></a>Propósito

Las aplicaciones aisladas y los ensamblados en paralelo son una solución de Microsoft Windows que reduce los conflictos de control de versiones en las aplicaciones cliente de Windows. Con Windows, los desarrolladores de aplicaciones pueden crear aplicaciones aisladas que son totalmente autodescriptivas y no se ven afectadas por los cambios en el registro, en otras aplicaciones o en otras versiones de los ensamblados que se ejecutan en el sistema. Los autores y los administradores de aplicaciones pueden usar manifiestos para administrar el uso compartido de ensamblados en paralelo después de la implementación en base o por aplicación. Los clientes se benefician de las aplicaciones aisladas que son más estables y se actualizan de forma más confiable.

## <a name="where-applicable"></a>Donde sea aplicable

Las aplicaciones aisladas y el uso compartido de ensamblados en paralelo se pueden usar para desarrollar aplicaciones que compartan de forma segura ensamblados del sistema operativo. Los desarrolladores pueden usar esta tecnología para corregir los conflictos de control de versiones de DLL causados por una versión incompatible de un ensamblado compartido.

Si su aplicación debe obtener sistemáticamente la versión de un componente que ha probado, es posible aislar la aplicación para que se ejecute siempre con la versión probada del componente en el equipo del usuario.

Las aplicaciones aisladas y los ensamblados en paralelo están diseñados para el desarrollo de aplicaciones de estilo de escritorio.

## <a name="developer-audience"></a>Audiencia de desarrolladores

Esta documentación está destinada principalmente a desarrolladores de software, desarrolladores de aplicaciones y administradores de red:

-   Los desarrolladores de software que desean crear aplicaciones aisladas que usarán los ensamblados en paralelo disponibles por Microsoft y otros publicadores de ensamblados en paralelo.
-   Los desarrolladores de aplicaciones interesados en crear sus propios ensamblados en paralelo para aislar sus aplicaciones.
-   Administradores de red que desean obtener más información sobre las aplicaciones aisladas.

Como referencia principal para el uso compartido de ensamblados en paralelo y aplicaciones aisladas, esta documentación proporciona información general sobre la creación de manifiestos y ensamblados en paralelo, la instalación de aplicaciones aisladas y ensamblados en paralelo, y el uso de la API de contexto de activación.

## <a name="run-time-requirements"></a>Requisitos de tiempo de ejecución

Se requiere Windows Server 2003 y versiones posteriores o Windows XP y versiones posteriores para usar ensamblados y manifiestos en paralelo para aislar las aplicaciones y usar la API de contexto de activación.

## <a name="in-this-section"></a>En esta sección



| Tema                                                         | Descripción                                                                    |
|---------------------------------------------------------------|--------------------------------------------------------------------------------|
| [Referencia](side-by-side-assemblies-reference.md)<br/> | Documentación de aplicaciones aisladas y ensamblados en paralelo.<br/> |



 

 

 




