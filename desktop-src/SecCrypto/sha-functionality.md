---
description: El proveedor base original comunicó incorrectamente que el algoritmo hash SHA enumera los algoritmos mediante llamadas a CryptGetProvParam con el parámetro PP \_ ENUMALGS especificado.
ms.assetid: 75128a4f-273a-4195-b206-30fc8bc589e9
title: Funcionalidad SHA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad8a06ce5c11dfaa00e2ec7ee3427dfda2f8b3ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808318"
---
# <a name="sha-functionality"></a>Funcionalidad SHA

El proveedor base original comunicó incorrectamente que el algoritmo hash [*Sha*](../secgloss/s-gly.md) enumera los algoritmos mediante llamadas a [**CryptGetProvParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetprovparam) con el parámetro PP \_ ENUMALGS especificado. Esto se ha corregido en el proveedor base. Tanto el proveedor base revisado como el proveedor extendido y ahora notifican correctamente a SHA-1.

Se ha \_ agregado una constante CALG SHA1 definida a Wincrypt. h con el mismo valor que CALG \_ Sha.

 

 
