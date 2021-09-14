---
description: Cada identificador de idioma se compone de un identificador de idioma principal que indica el idioma y un identificador de subidioma que indica el país o región.
ms.assetid: 8a6373e0-46c2-4b1b-bc67-543f426ef15a
title: Constantes y cadenas de identificador de lenguaje
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d80823e897a8325cbcb7207f91bde69397296767
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127063090"
---
# <a name="language-identifier-constants-and-strings"></a>Constantes y cadenas de identificador de lenguaje

> [!IMPORTANT]
> Las constantes de identificador de lenguaje están en desuso y no se recomienda su uso. Siempre es preferible usar nombres de configuración regional en lugar de identificadores de configuración regional.

Consulte [identificador de idioma](language-identifiers.md) para obtener una descripción de los identificadores de idioma.

Un identificador principal o de sublenguaje puede estar definido por el usuario o predefinido. Para obtener los identificadores de idioma principal predefinidos con sus identificadores de subidioma válidos, vea [[MS-LCID]: referencia](/openspecs/windows_protocols/ms-lcid/70feba9f-294e-491e-b6eb-56532684c37f)Windows identificador de código de lenguaje (LCID) .

> [!Note]  
> Si no hay ningún identificador de sublenguaje para usarlo con un identificador de idioma principal, la aplicación debe usar **SUBLANG \_ DEFAULT**. Debe usar **SUBLANG \_ NEUTRAL para** los recursos que son iguales para todos los sublenguajes de un idioma principal.

Un identificador de lenguaje principal definido por el usuario tiene un valor en el intervalo 0x0200 para 0x03ff. Todos los demás valores están reservados para su uso en el sistema operativo.

Un identificador de sublenguaje definido por el usuario tiene un valor en el intervalo 0x20 para 0x3f. Todos los demás valores están reservados para su uso en el sistema operativo.
