---
description: Directivas de sistema de usuario utilizadas con el Windows Installer.
ms.assetid: 74e940a1-dc7c-4ea3-ab62-d118204dac3e
title: Directivas de usuario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26cec4066e4d8267b2750d538e691d91382550fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907683"
---
# <a name="user-policies"></a>Directivas de usuario

Las siguientes directivas de usuario se pueden configurar en

**HKEY \_ \_** Directivas de software de usuario actual \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**



| Nombre del valor                                                            | Tipos de datos de valor          | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|-----------------------------------------------------------------------|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [AlwaysInstallElevated](alwaysinstallelevated.md)<br/>         | **\_valor DWORD reg**<br/> | Si este valor se establece en "1" y también se establece el valor del equipo correspondiente, el instalador siempre se instala con privilegios elevados.<br/> De lo contrario, el instalador usa privilegios elevados para instalar las aplicaciones administradas y usa el nivel de privilegios del usuario actual para las aplicaciones no administradas.<br/>                                                                                                                                                                                                      |
| [DisableMedia](disablemedia.md)<br/>                           | **\_valor DWORD reg**<br/> | Si la directiva [DisableMedia](disablemedia.md) se establece en "1", los usuarios y administradores que ejecuten una instalación de mantenimiento de un producto no podrán usar el cuadro de diálogo examinar para examinar los orígenes multimedia, como el CD-ROM, para los orígenes de otros productos instalables. La exploración de otros productos se impide, independientemente de si la instalación es con privilegios elevados. Todavía es posible que el usuario vuelva a instalar el producto desde el medio si el usuario tiene un origen de medios correctamente etiquetado.<br/> |
| [DisableRollback](disablerollback.md)<br/>                     | **\_valor DWORD reg**<br/> | Si este valor se establece en "1", el instalador no almacenará los archivos de reversión durante la instalación y se deshabilitará la reversión de la instalación. De forma predeterminada, la reversión está habilitada. Es aconsejable que los administradores no utilicen esta directiva a menos que sea absolutamente imprescindible.<br/>                                                                                                                                                                                                                                                             |
| [SearchOrder](searchorder.md)<br/>                             | **Registro \_ SZ**<br/>    | Orden en el que el instalador busca los tres tipos diferentes de orígenes:<br/> "n": red<br/> "m": medio (CD-ROM o DVD)<br/> "u": URL (localizador uniforme de recursos)<br/> Por ejemplo, un valor de "NMU" indica al instalador que busque primero los orígenes de red, los orígenes de medios segundo y los orígenes de direcciones URL en último lugar. Si se omite una letra, se quita el tipo de volumen correspondiente de la búsqueda. El orden predeterminado en ausencia de este valor es la red primero y luego el medio seguido de la dirección URL.<br/>          |
| [Directiva TransformsAtSource](transformsatsource-policy.md)<br/> | **\_valor DWORD reg**<br/> | Si este valor existe y está establecido en "1"; el instalador busca los archivos de transformación en la raíz de los orígenes de red en el [**SourceList**](sourcelist.md) del producto. De forma predeterminada, las transformaciones se almacenan en la carpeta datos de la aplicación del perfil de un usuario.<br/>                                                                                                                                                                                                                                             |



 

 

 




