---
title: Los archivos IDL y ACF
description: La sintaxis del Lenguaje de definición de interfaz de Microsoft (MIDL) se basa en la sintaxis del lenguaje de programación C. Cuando un concepto de lenguaje en esta descripción de MIDL no está totalmente definido, la definición del lenguaje C de ese término está implícita.
ms.assetid: f99f5934-750d-4c30-9970-803a891cacb7
keywords:
- Llamada a procedimiento remoto RPC, descrito, archivos IDL y ACF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9f7f739e50fd4e04ae35a11adcbbc936cd3cb36
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476579"
---
# <a name="the-idl-and-acf-files"></a>Los archivos IDL y ACF

La sintaxis del Lenguaje de definición de interfaz de Microsoft (MIDL) se basa en la sintaxis del lenguaje de programación C. Cuando un concepto de lenguaje en esta descripción de MIDL no está totalmente definido, la definición del lenguaje C de ese término está implícita.

El diseño MIDL especifica dos archivos distintos: el archivo del lenguaje de definición de interfaz (IDL) y el archivo de configuración de la aplicación (ACF). Estos archivos contienen atributos que dirigen la generación de los archivos de código auxiliar del lenguaje C que administran la llamada a procedimiento remoto (RPC). El archivo IDL contiene una descripción de la interfaz entre el cliente y los programas de servidor. Las aplicaciones RPC usan el archivo ACF para describir las características de la interfaz que son específicas del hardware y del sistema operativo que forma un entorno operativo determinado. El propósito de dividir esta información en dos archivos es mantener la interfaz de software independiente de las características que afectan solo al entorno operativo.

El archivo IDL especifica un contrato de red entre el cliente y el servidor, es decir, el archivo IDL especifica lo que se transmite entre el cliente y el servidor. Mantener esta información distinta de la información sobre el entorno operativo hace que el archivo IDL sea portátil a otros entornos. El archivo IDL consta de dos partes: un encabezado [de interfaz](the-idl-interface-header.md) y un cuerpo [de interfaz](the-idl-interface-body.md).

El ACF especifica atributos que afectan solo al rendimiento local en lugar del contrato de red. Rpc de Microsoft permite combinar los atributos ACF e IDL en un único archivo IDL. También puede combinar varias interfaces en un único archivo IDL (y su ACF).

En esta sección se resumen los atributos especificados en los archivos IDL y ACF. Está pensado para proporcionar solo información general. Para obtener información más detallada, vea la referencia [del lenguaje MIDL](/windows/desktop/Midl/midl-language-reference)y la referencia de Command-Line [MIDL.](/windows/desktop/Midl/midl-command-line-reference) La explicación de esta sección se presenta en los temas siguientes:

-   [El archivo del lenguaje de definición de interfaz (IDL)](the-interface-definition-language-idl-file.md)
-   [El archivo de configuración de la aplicación (ACF)](the-application-configuration-file-acf-.md)
-   [Salida del compilador MIDL](midl-compiler-output.md)

 

 