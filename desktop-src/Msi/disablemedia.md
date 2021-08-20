---
description: Si esta directiva de sistema por usuario se establece en &\# 0034;1&0034;, los usuarios y administradores que ejecutan una instalación de mantenimiento de un producto no podrán usar el cuadro de diálogo Examinar para examinar los orígenes multimedia, como CD-ROM, para los orígenes de otros productos \# instalables.
ms.assetid: 275a6d43-ecf8-4146-82eb-3b42b25b9a80
title: DisableMedia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2337a1698865b0b977e179021f6490e2fa651a8c4baa3a56e808d037926ad39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118143251"
---
# <a name="disablemedia"></a>DisableMedia

Si esta directiva [](system-policy.md) de sistema por usuario se establece en "1", se impide que los usuarios y administradores que ejecutan una instalación de mantenimiento de un producto usen el cuadro de diálogo Examinar para examinar los orígenes multimedia, como CD-ROM, para los orígenes de otros productos instalables. La exploración de otros productos se impide independientemente de si la instalación se realiza con privilegios elevados. Todavía es posible que el usuario vuelva a instalar el producto desde un medio si el usuario tiene un origen multimedia etiquetado correctamente.

## <a name="registry-key"></a>Clave del Registro

**HKEY \_ Directivas \_ de** \\ **software de USUARIO** \\ **ACTUAL** \\ **Instalador de** \\ **Windows** \\ **Microsoft**

## <a name="data-type"></a>Tipo de datos

**REG \_ DWORD**

## <a name="remarks"></a>Comentarios

Tenga en cuenta [**que la propiedad DISABLEMEDIA**](-disablemedia.md) tiene un efecto diferente al de la directiva DisableMedia. Al establecer la directiva del sistema DisableMedia, solo se deshabilita la exploración a orígenes multimedia. Establecer la **propiedad DISABLEMEDIA** impide que el instalador registre cualquier origen multimedia, como un CD-ROM, como origen válido para el producto. Sin embargo, si la exploración está habilitada, un usuario todavía puede ir a un origen multimedia.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Resistencia de origen](source-resiliency.md)
</dt> </dl>

 

 



