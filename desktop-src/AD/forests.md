---
title: Bosques
description: Un bosque es un conjunto de uno o varios árboles de dominio que no forman un espacio de nombres contiguo.
ms.assetid: b7beb305-0022-477a-85bf-779821202b26
ms.tgt_platform: multiple
keywords:
- bosques Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74ccccbce1c660c3f1e185e75971aa71d613c2db012ce42979cfaee7cd9c2b4b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118189214"
---
# <a name="forests"></a>Bosques

Un [*bosque*](/previous-versions/windows/desktop/legacy/ms681904(v=vs.85)) es un conjunto de uno o varios árboles de dominio que no forman un espacio de nombres contiguo. Todos los árboles de un bosque comparten un esquema, una configuración y un catálogo global comunes. Todos los árboles de una confianza de intercambio de bosque determinada de acuerdo con las relaciones de confianza jerárquicas transitivas de Kerberos. A diferencia de los árboles, un bosque no requiere un nombre distinto. Un bosque existe como un conjunto de objetos de referencia cruzada y relaciones de confianza de Kerberos reconocidas por los árboles miembros. Los árboles de un bosque forman una jerarquía para los fines de confianza de Kerberos; el nombre del árbol en la raíz del árbol de confianza hace referencia a un bosque determinado.

En la ilustración siguiente se muestra un bosque de espacios de nombres no contados.

![bosque de espacios de nombres no contados](images/forests.png)

 

 