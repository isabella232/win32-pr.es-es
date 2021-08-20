---
description: El BIOS virtual es una imagen de software que se carga en ram para configurar algunos de los aspectos básicos de y arrancar un sistema informático. Hay un elemento BIOS por sistema de equipo y ese elemento no se puede reemplazar ni quitar.
ms.assetid: EC691401-947F-4B56-A8A7-F0ECBF01677B
title: Clases de BIOS
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9605f28a23fc84b653ba5efe6c6e4be057eba48da81ddb777c7516d1317da6f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117813642"
---
# <a name="bios-classes"></a>Clases de BIOS

El BIOS virtual es una imagen de software que se carga en ram para configurar algunos de los aspectos básicos de y arrancar un sistema informático. Hay un elemento BIOS por sistema de equipo y ese elemento no se puede reemplazar ni quitar. Por lo tanto, no hay ningún grupo de recursos para agregar nuevos elementos bios a la máquina virtual. El elemento BIOS tampoco tiene su propia clase SettingData para describir la configuración del BIOS. Configuración para el BIOS, como los números de serie, el orden de arranque y el estado de bloqueo num, se encuentran en la clase [**Msvm \_ VirtualSystemSettingData.**](msvm-virtualsystemsettingdata.md)

Las siguientes son clases WMI de virtualización relacionadas con el BIOS. Estas clases están en \\ \\ . \\ Espacio de \\ nombres de virtualización raíz.

## <a name="in-this-section"></a>En esta sección



| Tema                                                    | Descripción                                                                                             |
|----------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| [**BIOSElement de Msvm \_**](msvm-bioselement.md)<br/> | Representa el software de bajo nivel que se carga en ram para configurar e iniciar el sistema.<br/> |
| [**Msvm \_ SystemBIOS**](msvm-systembios.md)<br/>   | Se usa para asociar una máquina virtual a su BIOS.<br/>                                           |



 

 

 




