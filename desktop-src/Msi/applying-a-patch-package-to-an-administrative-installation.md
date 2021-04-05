---
description: Puede aplicar la actualización pequeña a una imagen de origen administrativa de MNP2000.msi instalando la revisión de ejemplo MNP2000. MSP creada en la generación de un paquete de revisión.
ms.assetid: 24ae9cd6-2057-4345-90ec-943da7620cb0
title: Aplicar un paquete de revisión a una instalación administrativa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9e0645bdd2c472e725a3a5eeef22693aa35b8d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001750"
---
# <a name="applying-a-patch-package-to-an-administrative-installation"></a>Aplicar un paquete de revisión a una instalación administrativa

Puede aplicar la actualización pequeña a una imagen de origen administrativa de MNP2000.msi instalando la revisión de ejemplo MNP2000. MSP creada en la [generación de un paquete de revisión](generating-a-patch-package.md). La actualización se puede propagar a los usuarios solicitando que vuelvan a instalar la aplicación desde la nueva imagen de origen administrativa.

Un administrador puede usar la siguiente línea de comandos para actualizar la imagen de origen administrativa que se encuentra en//Server/MNP2000.msi a una nueva imagen de origen que sea igual que la que se produciría en una instalación administrativa desde un CD-ROM totalmente actualizado.

**msiexec/a//Server/MNP2000.msi/p MNP2000. MSP**

Los miembros del grupo de trabajo que usan MNP2000 deben volver a instalar la aplicación desde la nueva imagen de origen administrativa para recibir la actualización.

Para reinstalar completamente las aplicaciones y almacenar en caché el archivo. msi actualizado en el equipo del usuario, los usuarios pueden escribir cualquiera de los siguientes comandos.

**msiexec/fvomus//Server/MNP2000.msi**

**msiexec/I//Server/MNP2000.msi REINSTALL = ALL REINSTALLMODE = vomus**

Para reinstalar solo la característica de concierto actualizada y almacenar en caché el archivo. msi actualizado en el equipo del usuario, los usuarios pueden escribir el siguiente comando.

**msiexec/I//Server/MNP2000.msi REINSTALL = concierto REINSTALLMODE = vomus**

## <a name="next-example"></a>Ejemplo siguiente

[Un ejemplo de localización](a-localization-example.md)

 

 



