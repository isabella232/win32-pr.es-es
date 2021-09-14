---
description: Si esta directiva del sistema por usuario se establece en &\# 0034;1&0034;, los usuarios y administradores que ejecutan una instalación de mantenimiento de un producto no podrán usar el cuadro de diálogo Examinar para examinar los orígenes multimedia, como CD-ROM, para los orígenes de otros productos \# instalables.
ms.assetid: 275a6d43-ecf8-4146-82eb-3b42b25b9a80
title: DisableMedia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2ee50abf36225aa96e52332a53f0b2ab36f058c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127158543"
---
# <a name="disablemedia"></a>DisableMedia

Si esta directiva [](system-policy.md) de sistema por usuario se establece en "1", se impide que los usuarios y administradores que ejecutan una instalación de mantenimiento de un producto usen el cuadro de diálogo Examinar para examinar los orígenes multimedia, como CD-ROM, para los orígenes de otros productos instalables. La exploración de otros productos se impide independientemente de si la instalación se realiza con privilegios elevados. Todavía es posible que el usuario vuelva a instalar el producto desde medios si el usuario tiene un origen multimedia etiquetado correctamente.

## <a name="registry-key"></a>Clave del Registro

**HKEY \_ Directivas \_ de** \\ **software de USUARIO** \\ **ACTUAL** \\ **Instalador de** \\ **Windows** \\ **Microsoft**

## <a name="data-type"></a>Tipo de datos

**REG \_ DWORD**

## <a name="remarks"></a>Observaciones

Tenga en cuenta [**que la propiedad DISABLEMEDIA**](-disablemedia.md) tiene un efecto diferente al de la directiva DisableMedia. Al establecer la directiva del sistema DisableMedia, solo se deshabilita la exploración a orígenes multimedia. Establecer la **propiedad DISABLEMEDIA** impide que el instalador registre cualquier origen multimedia, como un CD-ROM, como origen válido para el producto. Sin embargo, si la exploración está habilitada, un usuario todavía puede ir a un origen multimedia.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Resistencia de origen](source-resiliency.md)
</dt> </dl>

 

 



