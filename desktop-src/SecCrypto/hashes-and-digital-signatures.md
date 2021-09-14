---
description: Con las funciones hash y firma digital, un usuario puede firmar digitalmente los datos para que cualquier otro usuario pueda comprobar que los datos no se han cambiado desde que se firmaron. También se puede comprobar la identidad del usuario que firmó los datos.
ms.assetid: dbe70506-f0d9-4239-a3af-8494fd6d4149
title: Hashes y firmas digitales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9dc2894cbf53834551afef375fb5056df89675a9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127265380"
---
# <a name="hashes-and-digital-signatures"></a>Hashes y firmas digitales

Con [las funciones hash y de](cryptography-functions.md)firma digital , un usuario puede firmar digitalmente los datos para que cualquier otro usuario pueda comprobar que los datos no se han cambiado desde que se firmaron. También se puede comprobar la identidad del usuario que firmó los datos.

Una [*firma digital*](../secgloss/d-gly.md) consta de una pequeña cantidad de datos binarios, normalmente menos de 256 bytes. Esta firma se puede agrupar con el mensaje firmado o almacenarse por separado, en función de cómo se haya implementado una aplicación determinada.

El proveedor de servicios criptográficos fuerte de Microsoft crea firmas digitales que se ajustan a rsa [*public key cryptography Standards*](../secgloss/p-gly.md) (PKCS) \# 1.

 

 
