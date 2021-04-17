---
description: Con las funciones de firma digital y hash, un usuario puede firmar digitalmente los datos para que cualquier otro usuario pueda comprobar que los datos no se han modificado desde que se firmó. También se puede comprobar la identidad del usuario que firmó los datos.
ms.assetid: dbe70506-f0d9-4239-a3af-8494fd6d4149
title: Hashes y firmas digitales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9dc2894cbf53834551afef375fb5056df89675a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668219"
---
# <a name="hashes-and-digital-signatures"></a>Hashes y firmas digitales

Con [las funciones de firma digital y hash](cryptography-functions.md), un usuario puede firmar digitalmente los datos para que cualquier otro usuario pueda comprobar que los datos no se han modificado desde que se firmó. También se puede comprobar la identidad del usuario que firmó los datos.

Una [*firma digital*](../secgloss/d-gly.md) consta de una pequeña cantidad de datos binarios, normalmente menos de 256 bytes. Esta firma se puede empaquetar con el mensaje firmado o almacenarse por separado, en función de cómo se haya implementado una aplicación determinada.

El proveedor de servicios criptográficos seguros de Microsoft crea firmas digitales que cumplen con los [*estándares de criptografía de clave pública*](../secgloss/p-gly.md) (PKCS) 1 de RSA \# .

 

 
