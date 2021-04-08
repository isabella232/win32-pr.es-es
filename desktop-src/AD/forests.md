---
title: Bosques
description: Un bosque es un conjunto de uno o más árboles de dominio que no forman un espacio de nombres contiguo.
ms.assetid: b7beb305-0022-477a-85bf-779821202b26
ms.tgt_platform: multiple
keywords:
- bosques Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc84fca35ce90b20582bd62a675e6cf8d0285f7e
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "103995084"
---
# <a name="forests"></a>Bosques

Un [*bosque*](/previous-versions/windows/desktop/legacy/ms681904(v=vs.85)) es un conjunto de uno o más árboles de dominio que no forman un espacio de nombres contiguo. Todos los árboles de un bosque comparten un esquema, una configuración y un catálogo global comunes. Todos los árboles de un bosque determinado confían en la confianza de acuerdo con las relaciones de confianza de Kerberos jerárquicas transitivas. A diferencia de los árboles, un bosque no requiere un nombre distinto. Un bosque existe como un conjunto de objetos de referencias cruzadas y relaciones de confianza de Kerberos que reconocen los árboles de miembros. Los árboles de un bosque forman una jerarquía para los fines de la confianza Kerberos; el nombre del árbol situado en la raíz del árbol de confianza hace referencia a un bosque determinado.

En la ilustración siguiente se muestra un bosque de espacios de nombres no contiguos.

![bosque de espacios de nombres no contiguos](images/forests.png)

 

 