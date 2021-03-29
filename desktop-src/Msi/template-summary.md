---
description: En el caso de un paquete de instalación, la propiedad de Resumen de la plantilla indica las versiones de plataforma y de idioma que son compatibles con esta base de datos de instalación.
ms.assetid: a1015ddb-8d5c-40f7-97ac-4a1347644ae6
title: Propiedad de Resumen de plantilla
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36b3949e7028fd0b1b5f9ff3112f1a3d03c9b87e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679281"
---
# <a name="template-summary-property"></a>Propiedad de Resumen de plantilla

En el caso de un paquete de instalación, la propiedad de Resumen de la **plantilla** indica las versiones de plataforma y de idioma que son compatibles con esta base de datos de instalación. La sintaxis de la información de la propiedad de Resumen de la **plantilla** para una base de datos de instalación es la siguiente:

\[*propiedad Platform* \] ; \[ *identificador* \] \[ de idioma,,... de *identificador de idioma* \] \[ \] .

Los ejemplos siguientes son valores válidos para la propiedad de **Resumen de plantilla** :

-   x64; 1033
-   Intel; 1033
-   Intel64; 1033
-   ; 1033
-   Intel; 1033, 2046
-   Intel64; 1033, 2046
-   Intel; 0
-   ARM; 1033, 2046
-   ARM; 0
-   Arm64; 1033, 2046
-   Arm64; 0

La propiedad **Resumen de plantilla** de una transformación indica las versiones de plataforma y de idioma compatibles con la transformación. En un archivo de transformación, solo se puede especificar un idioma. La plataforma y el idioma especificados determinan si una transformación puede aplicarse a una base de datos determinada. La propiedad Platform y la propiedad Language se pueden dejar en blanco si no se basa ninguna restricción de transformación para validar la transformación.

La propiedad de **Resumen de plantilla** de un paquete de revisión es una lista delimitada por signos de punto y coma de los códigos de producto que pueden aceptar la revisión. Si utiliza [Msimsp.exe](msimsp-exe.md) y [Patchwiz.dll](patchwiz-dll.md) para generar el paquete de revisión, esta lista se obtiene de la [tabla TargetImages](targetimages-table-patchwiz-dll-.md) del archivo de creación de la revisión.

Esta propiedad de resumen es obligatoria.

## <a name="remarks"></a>Observaciones

Si la plataforma actual no coincide con una de las plataformas especificadas en la propiedad de **Resumen de plantilla** , el instalador no procesa el paquete.

Si falta la especificación de la plataforma en el valor de propiedad de Resumen de la **plantilla** , el instalador asume la arquitectura de Intel.

Si se trata de un paquete de Windows Installer de 64 bits que se ejecuta en una plataforma Intel64 (Itanium), escriba Intel64 en la propiedad Resumen de la **plantilla** .

Si se trata de un paquete de Windows Installer de 64 bits que se ejecuta en una plataforma x64, escriba x64 en la propiedad Resumen de la **plantilla** .

Si se trata de un paquete de Windows Installer de 64 bits que se ejecuta en una plataforma Arm64, escriba Arm64 en la propiedad Resumen de la **plantilla** .

No se puede marcar un paquete de Windows Installer como compatible con Intel64 y x64; por ejemplo, el valor de la propiedad Summary de la **plantilla** de Intel64, x64 no es válido.

No se puede marcar un paquete de Windows Installer como compatible con plataformas de 32 bits y de 64 bits; por ejemplo, los valores de propiedad de **Resumen de plantilla** como Intel, x64 o Intel, Intel64 no son válidos.

Si escribe 0 (cero) en el campo ID. de idioma de la propiedad Resumen de la **plantilla** o si se mantiene este campo vacío, indica que el paquete es independiente del idioma.

Si se trata de un paquete de Windows Installer que se ejecuta en Windows RT, escriba el valor ARM en la propiedad de Resumen de la **plantilla** .

Los módulos de fusión mediante combinación son los únicos paquetes que pueden tener varios idiomas. Solo se puede especificar un idioma en una base de datos del instalador de origen. Para obtener más información, vea [módulos de combinación en varios idiomas](multiple-language-merge-modules.md).

La plataforma Alpha no es compatible con Windows Installer.

**Windows Installer:** No se admite la sintaxis siguiente:

\[*propiedad Platform* \] \[ ,*propiedad Platform* \] \[ \] ,... \[ *identificador* \] \[ de idioma,,... de *identificador de idioma* \] \[ \] .

Los ejemplos siguientes no son valores válidos para la propiedad de **Resumen de plantilla** :

-   Alpha, Intel; 1033
-   Intel, Alpha; 1033
-   Alfa; 1033
-   Alpha; 1033, 2046

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Descripciones de propiedades de Resumen](summary-property-descriptions.md)
</dt> </dl>

 

 




