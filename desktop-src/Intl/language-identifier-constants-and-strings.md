---
description: Cada identificador de idioma se compone de un identificador de idioma principal que indica el idioma y un identificador de idioma que indica el país o región.
ms.assetid: 8a6373e0-46c2-4b1b-bc67-543f426ef15a
title: Constantes y cadenas de identificador de idioma
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d80823e897a8325cbcb7207f91bde69397296767
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104360807"
---
# <a name="language-identifier-constants-and-strings"></a>Constantes y cadenas de identificador de idioma

> [!IMPORTANT]
> Las constantes de identificador de idioma están desusadas y no se recomienda su uso. Siempre se prefiere el uso de nombres de configuración regional en lugar de los identificadores de configuración regional.

Vea [identificador de idioma](language-identifiers.md) para obtener una descripción de los identificadores de idioma.

Un identificador principal o de subidioma puede estar definido por el usuario o ser predefinido. Para los identificadores de idioma principal predefinidos con sus identificadores de subidioma válidos, vea [[ms-LCID]: referencia de identificador de idioma de Windows (LCID)](/openspecs/windows_protocols/ms-lcid/70feba9f-294e-491e-b6eb-56532684c37f).

> [!Note]  
> Si no hay ningún identificador de subidioma para usar con un identificador de idioma principal, la aplicación debe usar el **\_ valor predeterminado de sublang**. Debe usar el **sublang \_ neutro** para los recursos que son iguales para todos los subidiomas de un idioma principal.

Un identificador de idioma principal definido por el usuario tiene un valor en el intervalo de 0x0200 a 0x03ff. Todos los demás valores están reservados para el uso del sistema operativo.

Un identificador de subidioma definido por el usuario tiene un valor en el intervalo de 0x20 a 0x3F. Todos los demás valores están reservados para el uso del sistema operativo.
