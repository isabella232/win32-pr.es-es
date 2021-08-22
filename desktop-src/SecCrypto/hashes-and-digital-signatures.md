---
description: Con las funciones hash y de firma digital, un usuario puede firmar digitalmente los datos para que cualquier otro usuario pueda comprobar que los datos no se han cambiado desde que se firmaron. También se puede comprobar la identidad del usuario que firmó los datos.
ms.assetid: dbe70506-f0d9-4239-a3af-8494fd6d4149
title: Hashes y firmas digitales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdd6367217343a067bbdd0d5a4ad5e9f4f47e9b744ee9f159046259ec2e26185
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006493"
---
# <a name="hashes-and-digital-signatures"></a>Hashes y firmas digitales

Con las funciones hash y de firma [digital,](cryptography-functions.md)un usuario puede firmar digitalmente los datos para que cualquier otro usuario pueda comprobar que los datos no se han cambiado desde que se firmaron. También se puede comprobar la identidad del usuario que firmó los datos.

Una [*firma digital*](../secgloss/d-gly.md) consta de una pequeña cantidad de datos binarios, normalmente de menos de 256 bytes. Esta firma se puede agrupar con el mensaje firmado o almacenarse por separado, en función de cómo se haya implementado una aplicación determinada.

El proveedor de servicios criptográficos fuerte de Microsoft crea firmas digitales que se ajustan a [*los*](../secgloss/p-gly.md) estándares de criptografía de clave pública RSA (PKCS) \# 1.

 

 
