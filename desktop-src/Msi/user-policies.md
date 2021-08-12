---
description: Directivas del sistema de usuario que se usan con Windows Instalador.
ms.assetid: 74e940a1-dc7c-4ea3-ab62-d118204dac3e
title: Directivas de usuario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31ce52f4a691729c71ed57ddba8dd80811681844e1ba6c02664ee50c11f8d0e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118623094"
---
# <a name="user-policies"></a>Directivas de usuario

Las siguientes directivas de usuario se pueden configurar en

**HKEY \_ Directivas \_ de** \\ **software de USUARIO** \\ **ACTUAL** \\ **Instalador de** \\ **Windows** \\ **Microsoft**



| Nombre del valor                                                            | Tipos de datos de valor          | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|-----------------------------------------------------------------------|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [AlwaysInstallElevated](alwaysinstallelevated.md)<br/>         | **REG \_ DWORD**<br/> | Si este valor se establece en "1" y también se establece el valor de equipo correspondiente, el instalador siempre se instala con privilegios elevados.<br/> De lo contrario, el instalador usa privilegios elevados para instalar aplicaciones administradas y usa el nivel de privilegios del usuario actual para las aplicaciones no administradas.<br/>                                                                                                                                                                                                      |
| [DisableMedia](disablemedia.md)<br/>                           | **REG \_ DWORD**<br/> | Si la directiva [DisableMedia](disablemedia.md) está establecida en "1", se impide que los usuarios y administradores que ejecutan una instalación de mantenimiento de un producto usen el cuadro de diálogo Examinar para examinar los orígenes multimedia, como CD-ROM, para los orígenes de otros productos instalables. La exploración de otros productos se impide independientemente de si la instalación tiene privilegios elevados. Todavía es posible que el usuario vuelva a instalar el producto desde un medio si el usuario tiene un origen multimedia etiquetado correctamente.<br/> |
| [DisableRollback](disablerollback.md)<br/>                     | **REG \_ DWORD**<br/> | Si este valor se establece en "1", el instalador no almacenará los archivos de reversión durante la instalación, lo que deshabilita la reversión de la instalación. De forma predeterminada, la reversión está habilitada. Se recomienda a los administradores no usar esta directiva a menos que sea absolutamente esencial.<br/>                                                                                                                                                                                                                                                             |
| [SearchOrder](searchorder.md)<br/>                             | **REG \_ SZ**<br/>    | Orden en el que el instalador busca en los tres tipos diferentes de orígenes:<br/> "n": red<br/> "m": medios (CD-ROM o DVD)<br/> "u": dirección URL (localizador uniforme de recursos)<br/> Por ejemplo, un valor de "nmu" indica al instalador que busque primero los orígenes de red, los orígenes multimedia en segundo lugar y los orígenes de dirección URL en último lugar. Si se deja una letra, se quita el tipo de volumen correspondiente de la búsqueda. El orden predeterminado en ausencia de este valor es primero la red y, a continuación, el medio seguido de la dirección URL.<br/>          |
| [Directiva TransformsAtSource](transformsatsource-policy.md)<br/> | **REG \_ DWORD**<br/> | Si este valor existe y se establece en "1"; el instalador busca archivos de transformación en la raíz de los orígenes de red de la [**lista de orígenes**](sourcelist.md) del producto. De forma predeterminada, las transformaciones se almacenan en la carpeta Datos de aplicación del perfil de un usuario.<br/>                                                                                                                                                                                                                                             |



 

 

 




