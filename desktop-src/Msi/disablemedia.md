---
description: Si esta Directiva del sistema por usuario está establecida en &\# 0034; 1&\# 0034;, los usuarios y administradores que ejecuten una instalación de mantenimiento de un producto no podrán usar el cuadro de diálogo examinar para buscar orígenes multimedia, como un CD-ROM, para los orígenes de otros productos instalables.
ms.assetid: 275a6d43-ecf8-4146-82eb-3b42b25b9a80
title: DisableMedia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2ee50abf36225aa96e52332a53f0b2ab36f058c
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104003306"
---
# <a name="disablemedia"></a>DisableMedia

Si esta [Directiva del sistema](system-policy.md) por usuario se establece en "1", los usuarios y administradores que ejecuten una instalación de mantenimiento de un producto no podrán usar el cuadro de diálogo examinar para examinar los orígenes multimedia, como el CD-ROM, para los orígenes de otros productos instalables. La exploración de otros productos se evita independientemente de si la instalación se realiza con privilegios elevados. Todavía es posible que el usuario vuelva a instalar el producto desde el medio si el usuario tiene un origen de medios correctamente etiquetado.

## <a name="registry-key"></a>Clave del Registro

**HKEY \_ \_** Directivas de software de usuario actual \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Tipo de datos

**\_valor DWORD reg**

## <a name="remarks"></a>Observaciones

Tenga en cuenta que la propiedad [**DISABLEMEDIA**](-disablemedia.md) tiene un efecto distinto al de la Directiva DISABLEMEDIA. Al establecer la Directiva del sistema DisableMedia, solo se deshabilita la exploración de los orígenes multimedia. El establecimiento de la propiedad **DISABLEMEDIA** evita que el instalador registre cualquier origen multimedia, como un CD-ROM, como un origen válido para el producto. Sin embargo, si la exploración está habilitada, es posible que un usuario siga explorando un origen de medios.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Resistencia de origen](source-resiliency.md)
</dt> </dl>

 

 



