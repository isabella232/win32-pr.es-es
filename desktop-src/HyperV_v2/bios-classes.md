---
description: El BIOS virtual es una imagen de software que se carga en la RAM para configurar algunos de los aspectos básicos de y arrancar un equipo. Hay un elemento BIOS por sistema y ese elemento no se puede reemplazar ni quitar.
ms.assetid: EC691401-947F-4B56-A8A7-F0ECBF01677B
title: Clases de BIOS
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e725910bbeb1032f876b5e4fcf08da4a6ea60bc1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104002018"
---
# <a name="bios-classes"></a>Clases de BIOS

El BIOS virtual es una imagen de software que se carga en la RAM para configurar algunos de los aspectos básicos de y arrancar un equipo. Hay un elemento BIOS por sistema y ese elemento no se puede reemplazar ni quitar. Por lo tanto, no hay ningún grupo de recursos para agregar nuevos elementos BIOS a la máquina virtual. El elemento BIOS tampoco tiene su propia clase SettingData para describir la configuración del BIOS. La configuración del BIOS, como los números de serie, el orden de arranque y el estado de Bloq Num, se encuentra en la clase [**MSVM \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) .

A continuación se enumeran las clases WMI de virtualización relacionadas con el BIOS. Estas clases se encuentran en \\ \\ . \\ \\Espacio de nombres de virtualización de raíz.

## <a name="in-this-section"></a>En esta sección



| Tema                                                    | Descripción                                                                                             |
|----------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| [**MSVM \_ BIOSElement**](msvm-bioselement.md)<br/> | Representa el software de bajo nivel que se carga en la RAM para configurar e iniciar el sistema.<br/> |
| [**MSVM \_ SystemBIOS**](msvm-systembios.md)<br/>   | Se usa para asociar una máquina virtual a su BIOS.<br/>                                           |



 

 

 




