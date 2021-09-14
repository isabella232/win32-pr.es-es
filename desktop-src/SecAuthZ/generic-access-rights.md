---
description: Los objetos protegibles usan un formato de máscara de acceso en el que los cuatro bits de orden superior especifican derechos de acceso genéricos.
ms.assetid: e18cede9-9bf7-4866-850b-5d7fa43a5b0f
title: Derechos de acceso genéricos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adff14aa259222bc37096b8a94f30cffb5ab0876
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069118"
---
# <a name="generic-access-rights"></a>Derechos de acceso genéricos

Los objetos protegibles usan un [formato de máscara de acceso](access-mask-format.md) en el que los cuatro bits de orden superior especifican derechos de acceso genéricos. Cada tipo de objeto protegible asigna estos bits a un conjunto de sus derechos de acceso estándar y específicos del objeto. Por ejemplo, un objeto de archivo Windows asigna el bit DE LECTURA GENÉRICA a los derechos de acceso estándar READ CONTROL y SYNCHRONIZE y a los derechos de acceso específicos del objeto FILE READ DATA, FILE READ EA y \_ FILE \_ READ \_ \_ \_ \_ \_ \_ ATTRIBUTES. Otros tipos de objetos asignan el bit GENERIC READ a cualquier conjunto de derechos \_ de acceso adecuado para ese tipo de objeto.

Puede usar derechos de acceso genéricos para especificar el tipo de acceso que necesita al abrir un identificador para un objeto . Esto suele ser más sencillo que especificar todos los derechos estándar y específicos correspondientes.

En la tabla siguiente se muestran las constantes definidas para los derechos de acceso genéricos.



| Constante         | Significado genérico            |
|------------------|----------------------------|
| GENERIC \_ ALL     | Todos los derechos de acceso posibles |
| GENERIC \_ EXECUTE | Ejecución del acceso             |
| LECTURA \_ GENÉRICA    | acceso de lectura                |
| ESCRITURA \_ GENÉRICA   | Acceso de escritura               |



 

Las aplicaciones que definen objetos protegibles privados también pueden usar los derechos de acceso genéricos.

 

 



