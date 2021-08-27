---
description: Cada identificador de idioma se compone de un identificador de idioma principal que indica el idioma y un identificador de subidioma que indica el país o región.
ms.assetid: 8a6373e0-46c2-4b1b-bc67-543f426ef15a
title: Constantes y cadenas de identificador de idioma
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67321097d93c5f4224a86a66528f98dacce18312003062665ccc30c1377de70f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118948752"
---
# <a name="language-identifier-constants-and-strings"></a>Constantes y cadenas de identificador de idioma

> [!IMPORTANT]
> Las constantes de identificador de idioma están en desuso y no se recomienda su uso. Siempre es preferible usar nombres de configuración regional en lugar de identificadores de configuración regional.

Consulte [identificador de idioma](language-identifiers.md) para obtener una descripción de los identificadores de idioma.

Un identificador principal o de subidioma puede estar definido por el usuario o predefinido. Para obtener los identificadores de idioma principal predefinidos con sus identificadores de sublenguaje válidos, vea [[MS-LCID]: Windows Language Code Identifier (LCID) Reference](/openspecs/windows_protocols/ms-lcid/70feba9f-294e-491e-b6eb-56532684c37f).

> [!Note]  
> Si no hay ningún identificador de subidioma para usar con un identificador de idioma principal, la aplicación debe usar **SUBLANG \_ DEFAULT**. Debe usar **SUBLANG \_ NEUTRAL para** los recursos que son iguales para todos los sublenguajes de un idioma principal.

Un identificador de idioma principal definido por el usuario tiene un valor en el intervalo 0x0200 para 0x03ff. Todos los demás valores están reservados para su uso en el sistema operativo.

Un identificador de subidioma definido por el usuario tiene un valor en el intervalo 0x20 para 0x3f. Todos los demás valores están reservados para su uso en el sistema operativo.
