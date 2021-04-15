---
description: Algoritmos admitidos por Microsoft base DSS y Diffie-Hellman proveedor de servicios criptográficos.
ms.assetid: 8db1c7cb-41e0-470b-b927-989da4c09324
title: Algoritmos de proveedor de PROV_DSS_DH
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 098625153d4d447d7290827dcad44a6c78f55561
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105649287"
---
# <a name="prov_dss_dh-provider-algorithms"></a>\_Algoritmos de proveedor de DSS DSS \_ DH

En la tabla siguiente se enumeran los algoritmos admitidos por Microsoft base DSS y Diffie-Hellman proveedor de servicios criptográficos.



| IDENTIFICADOR de algoritmo      | Descripción                                 | Comentarios                                                                                                        |
|-------------------|---------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| CALG \_ MD5         | Algoritmo de hash MD5.                      | Solo se proporciona para el hash.                                                                                      |
| CALG \_ Sha         | Algoritmo de hash SHA.                      | Debe usarse para las firmas de DSS.                                                                                |
| CALG \_ SHA1        | Igual que CALG \_ Sha.                          | Sin comentarios.                                                                                                     |
| \_firma DSS de CALG \_   | Algoritmo de firma de clave pública y privada de DSS. | Longitud de clave: se puede establecer, de 512 bits a 1.024 bits en incrementos de 64 bits. Longitud de clave predeterminada: 1.024 bits.<br/> |
| CALG \_ DH \_ SF      | Almacenar y reenviar el intercambio de claves D-H.         | Longitud de clave: se puede establecer, de 384 bits a 512 bits en incrementos de 8 bits. Longitud de clave predeterminada: 512 bits.<br/>      |
| CALG \_ DH \_ EPHEM   | Intercambio de claves en D-H efímero.                 | Longitud de clave: se puede establecer, de 384 bits a 512 bits en incrementos de 8 bits. Longitud de clave predeterminada: 512 bits.<br/>      |
| CALG \_ CYLINK \_ clave MEK | Una variante de 40 bits de una clave DES.              | Longitud de clave: 40 bits.                                                                                            |



 

 

 




