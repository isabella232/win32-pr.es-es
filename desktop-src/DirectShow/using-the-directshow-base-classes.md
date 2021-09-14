---
description: Uso de las DirectShow base
ms.assetid: 7eab0e55-1566-4b4c-b37c-32c5a1f37363
title: Uso de las DirectShow base
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 870c910505d6df42d0b9a6094470bf803b83d6b9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126891625"
---
# <a name="using-the-directshow-base-classes"></a>Uso de las DirectShow base

Para usar las clases base en DirectShow, debe compilar y vincular la biblioteca de clases base.

La biblioteca de clases base se proporciona como un ejemplo de SDK en microsoft Windows Software Development Kit (SDK) ( <https://go.microsoft.com/fwlink/p/?linkid=62332> ). La ubicación exacta depende de la versión del SDK que haya instalado, pero la ruta de acceso relativa es:

*(Raíz de ejemplos del SDK)* \\ \\DirectShow BaseClasses

Encabezado: Secuencias.h

Biblioteca: el ejemplo compila versiones comerciales y de depuración de la biblioteca:

-   Versión comercial: Strmbase.lib
-   Versión de depuración: Strmbasd.lib.

Para obtener más información sobre cómo configurar el entorno de compilación, vea [Configurar el entorno de compilación.](setting-up-the-build-environment.md)

## <a name="preprocessor-symbols"></a>Símbolos de preprocesador

Al incluir el archivo de encabezado Secuencias.h, los siguientes símbolos de preprocesador tienen un significado especial:

-   PERF: reservado. No use este símbolo de preprocesador.
-   VFWROBUST: habilita la validación de punteros en el comercio minorista. Para obtener más información, vea [Macros de validación de puntero.](pointer-validation-macros.md) En las compilaciones de depuración, no es necesario definir VFWROBUST.

> [!Note]  
> En Windows Vista y versiones posteriores, las macros de validación de puntero están vacías.

 

 

 



