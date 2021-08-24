---
description: Para un paquete de instalación, la propiedad Resumen de plantilla indica las versiones de plataforma y lenguaje compatibles con esta base de datos de instalación.
ms.assetid: a1015ddb-8d5c-40f7-97ac-4a1347644ae6
title: Propiedad Resumen de plantilla
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da93d2d3a38f3c1853f3f936fe6f97b8550dcaeac70d4b553b8cb0362f41ee41
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119893455"
---
# <a name="template-summary-property"></a>Propiedad Resumen de plantilla

Para un paquete de instalación, la **propiedad Resumen** de plantilla indica las versiones de plataforma y lenguaje compatibles con esta base de datos de instalación. La sintaxis de la **información de la propiedad Resumen** de plantilla para una base de datos de instalación es la siguiente:

\[*platform, propiedad* \] ; \[ *language id* \] \[ , language id *,...* \] \[ \] .

Los ejemplos siguientes son valores válidos para la **propiedad Resumen de** plantilla:

-   x64;1033
-   Intel;1033
-   Intel64;1033
-   ;1033
-   Intel ;1033,2046
-   Intel64;1033,2046
-   Intel;0
-   Arm;1033,2046
-   Arm;0
-   Arm64;1033,2046
-   Arm64;0

La **propiedad Resumen de plantilla** de una transformación indica las versiones de plataforma y lenguaje compatibles con la transformación. En un archivo de transformación, solo se puede especificar un idioma. La plataforma y el lenguaje especificados determinan si una transformación se puede aplicar a una base de datos determinada. La propiedad de plataforma y la propiedad de lenguaje se pueden dejar en blanco si ninguna restricción de transformación se basa en ellos para validar la transformación.

La **propiedad Resumen de plantilla** de un paquete de revisión es una lista delimitada por punto y coma de los códigos de producto que pueden aceptar la revisión. Si usa [Msimsp.exe](msimsp-exe.md) y [Patchwiz.dll](patchwiz-dll.md) para generar el paquete de revisión, esta lista se obtiene de la tabla [TargetImages](targetimages-table-patchwiz-dll-.md) del archivo de creación de revisiones.

Esta propiedad de resumen es obligatoria.

## <a name="remarks"></a>Comentarios

Si la plataforma actual no coincide con una de las plataformas especificadas en la propiedad **Resumen** de plantilla, el instalador no procesa el paquete.

Si falta la especificación de la plataforma en el **valor de la** propiedad Resumen de plantilla, el instalador asume la arquitectura de Intel.

Si se trata de un paquete de instalador de Windows de 64 bits que se ejecuta en una plataforma Intel64 (Itanium), escriba Intel64 en la propiedad **Resumen** de plantilla.

Si se trata de un paquete de instalador de Windows de 64 bits que se ejecuta en una plataforma x64, escriba x64 en la **propiedad Resumen de** plantilla.

Si se trata de un paquete de instalador de Windows de 64 bits que se ejecuta en una plataforma arm64, escriba Arm64 en la **propiedad Resumen de** plantilla.

Un Windows installer no se puede marcar como compatible con Intel64 y x64; Por ejemplo, el **valor de la** propiedad Resumen de plantilla de Intel64,x64 no es válido.

Un Windows installer no se puede marcar como compatible con las plataformas de 32 y 64 bits; Por ejemplo, **los valores de propiedad Resumen** de plantilla, como Intel,x64 o Intel,Intel64, no son válidos.

Si escribe 0 (cero) en el campo id. de idioma de la propiedad **Resumen** de plantilla o deja este campo vacío, indica que el paquete es neutro en el idioma.

Si se trata de un Windows installer que se ejecuta en Windows RT, escriba el valor Arm en la **propiedad Resumen de** plantilla.

Los módulos de combinación son los únicos paquetes que pueden tener varios idiomas. Solo se puede especificar un idioma en una base de datos del instalador de origen. Para obtener más información, vea [Módulos de combinación de varios lenguajes.](multiple-language-merge-modules.md)

La plataforma Alfa no es compatible con Windows Instalador.

**Windows instalador:** No se admite la sintaxis siguiente:

\[*propiedad de plataforma* \] \[ , propiedad *de* \] \[ ,... \] \[ *language id* \] \[ , language id *,...* \] \[ \] .

Los ejemplos siguientes no son valores válidos para la **propiedad Resumen de** plantilla:

-   Alpha,Intel;1033
-   Intel,Alpha;1033
-   Alpha;1033
-   Alpha;1033,2046

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Instalador 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Resumen de descripciones de propiedades](summary-property-descriptions.md)
</dt> </dl>

 

 




