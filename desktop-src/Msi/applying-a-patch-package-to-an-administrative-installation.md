---
description: Puede aplicar la pequeña actualización a una imagen de origen administrativa de MNP2000.msi instalando la revisión de ejemplo MNP2000.msp creada en Generar un paquete de revisión.
ms.assetid: 24ae9cd6-2057-4345-90ec-943da7620cb0
title: Aplicar un paquete de revisión a una instalación administrativa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9e0645bdd2c472e725a3a5eeef22693aa35b8d3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159126"
---
# <a name="applying-a-patch-package-to-an-administrative-installation"></a>Aplicar un paquete de revisión a una instalación administrativa

Puede aplicar la pequeña actualización a una imagen de origen administrativo de MNP2000.msi instalando la revisión de ejemplo MNP2000.msp creada en Generar un paquete [de revisión](generating-a-patch-package.md). A continuación, la actualización se puede propagar a los usuarios solicitando que vuelvan a instalar la aplicación desde la nueva imagen de origen administrativa.

Un administrador puede usar la siguiente línea de comandos para actualizar la imagen de origen administrativa ubicada en //server/MNP2000.msi a una nueva imagen de origen que sea la misma que produciría una instalación administrativa desde un CD-ROM totalmente actualizado.

**msiexec /a //server/MNP2000.msi /p MNP2000.msp**

Los miembros del grupo de trabajo que usan MNP2000 deben reinstalar la aplicación desde la nueva imagen de origen administrativo para recibir la actualización.

Para reinstalar completamente las aplicaciones y almacenar en caché el archivo .msi actualizado en el equipo del usuario, los usuarios pueden escribir cualquiera de los siguientes comandos.

**msiexec /fvomus //server/MNP2000.msi**

**msiexec /I //server/MNP2000.msi REINSTALL=ALL REINSTALLMODE=vomus**

Para reinstalar solo la característica Concert actualizada y almacenar en caché el archivo .msi actualizado en el equipo del usuario, los usuarios pueden escribir el siguiente comando.

**msiexec /I //server/MNP2000.msi REINSTALL=Concert REINSTALLMODE=vomus**

## <a name="next-example"></a>Ejemplo siguiente

[Ejemplo de localización](a-localization-example.md)

 

 



