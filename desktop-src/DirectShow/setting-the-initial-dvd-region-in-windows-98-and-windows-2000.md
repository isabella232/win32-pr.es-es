---
description: Establecimiento de la región de DVD inicial
ms.assetid: b8238cb4-a101-4998-866f-4cf9ebd5d277
title: Establecimiento de la región de DVD inicial
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7bf019c7d5ddae8efb257435e1b23037575a37f809ef012190b49c619cc3211
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120102325"
---
# <a name="setting-the-initial-dvd-region"></a>Establecimiento de la región de DVD inicial

Es responsabilidad del fabricante del sistema seleccionar una región de DVD inicial para la unidad de DVD en sus equipos.

> [!Note]  
> Solo se pueden usar discos cifrados para establecer la región.

 

### <a name="windows-2000-and-later"></a>Windows 2000 y versiones posteriores

A partir Windows 2000, la región de DVD predeterminada se selecciona en función de la configuración regional para la que está configurada la máquina. Windows 2000 siempre establecerá la región inicial de una unidad de DVD con esta región predeterminada, así como la región del disco, si hay un disco en la unidad. El fabricante del sistema no tiene que hacer nada para establecer la región inicial Windows 2000 unidades de DVD o posteriores.

En el caso de las unidades RPC1, si no hay ningún disco en la unidad durante el arranque, la región predeterminada se establece solo en función de la configuración regional de la máquina. Si hay un disco de DVD en la unidad durante el arranque, se selecciona la región predeterminada para que sea la región de la unidad, siempre que coincida con una región del disco. De lo contrario, la región más baja del disco se selecciona como la región inicial de la unidad. El usuario (o fabricante del sistema) tiene un cambio restante permitido, en caso de que el valor predeterminado no sea correcto.

En el caso de las unidades RPC2, si durante el proceso de instalación Windows 2000 encuentra que la unidad no tiene ninguna región establecida, intentará elegir una región como se ha indicado anteriormente, pero solo si hay un disco en la unidad. (Las unidades RPC1 elegirán la región sin ningún disco en la unidad). Una vez que se establece una región para las unidades RPC2, no se cambia automáticamente mediante una nueva instalación o una instalación limpia del sistema operativo.

El OEM puede establecer una clave del Registro que contenga la región de DVD predeterminada para el sistema. En el primer arranque, la región de la unidad se establecerá en este valor. La clave del Registro Windows 2000 y versiones posteriores es HKLM \\ System \\ CurrentControlSet \\ Control Class \\ \\ <CDROM GUID> \\ <instance number> \\ DefaultDVDRegion(binary) .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Compatibilidad con el cambio de región de DVD en Windows](dvd-region-change-support-in-windows.md)
</dt> </dl>

 

 



