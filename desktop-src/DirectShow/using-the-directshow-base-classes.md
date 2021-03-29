---
description: Usar las clases base de DirectShow
ms.assetid: 7eab0e55-1566-4b4c-b37c-32c5a1f37363
title: Usar las clases base de DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 870c910505d6df42d0b9a6094470bf803b83d6b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277589"
---
# <a name="using-the-directshow-base-classes"></a>Usar las clases base de DirectShow

Para usar las clases base en DirectShow, debe compilar y vincular la biblioteca de clases base.

La biblioteca de clases base se proporciona como un ejemplo de SDK en el kit de desarrollo de software (SDK) de Microsoft Windows ( <https://go.microsoft.com/fwlink/p/?linkid=62332> ). La ubicación exacta depende de la versión del SDK que haya instalado, pero la ruta de acceso relativa es:

*(Ejemplos del SDK raíz)* \\ BaseClasses de DirectShow \\

Encabezado: streams. h

Biblioteca: el ejemplo genera versiones comercial y de depuración de la biblioteca:

-   Versión comercial: Strmbase. lib
-   Versión de depuración: Strmbasd. lib.

Para obtener más información sobre cómo configurar el entorno de compilación, vea [configurar el entorno de compilación](setting-up-the-build-environment.md).

## <a name="preprocessor-symbols"></a>Símbolos de preprocesador

Cuando se incluye el archivo de encabezado streams. h, los siguientes símbolos de preprocesador tienen un significado especial:

-   RENDIMIENTO: reservado. No utilice este símbolo de preprocesador.
-   VFWROBUST: habilita la validación de puntero en la versión comercial. Para obtener más información, vea [macros de validación de punteros](pointer-validation-macros.md). En las compilaciones de depuración, no es necesario definir VFWROBUST.

> [!Note]  
> En Windows Vista y versiones posteriores, las macros de validación de puntero están vacías.

 

 

 



