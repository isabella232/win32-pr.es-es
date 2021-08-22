---
description: Para firmar un archivo y crear un catálogo para él, primero debe tener un proceso para firmar archivos, un certificado y una clave pública.
ms.assetid: 61337ea6-2d6b-4080-9128-5b8527512ce6
title: Crear archivos y catálogos firmados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf9abcccc2451cfa9461bc8129705c1094291b33fea609679c89ef46d7cf7348
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142328"
---
# <a name="creating-signed-files-and-catalogs"></a>Crear archivos y catálogos firmados

Para firmar un archivo y crear un catálogo para él, primero debe tener un proceso para firmar archivos, un certificado y una clave pública.

**Para firmar un archivo y crear un catálogo**

1.  Use [Pktextract.exe](pktextract-exe.md) para extraer el [*token de clave pública*](p-sbscs-gly.md) del archivo de certificado. El archivo de certificado debe estar presente en el mismo directorio que la utilidad .
2.  Use el valor del token de clave pública para actualizar el **atributo publicKeyToken** del **elemento assemblyIdentity** en el archivo de manifiesto.
3.  Use [MT.exe](mt-exe.md) para generar hashes de archivos contenidos en el manifiesto del ensamblado y para crear el archivo de descripción del catálogo (.cdf).
4.  Use Makecat.exe con el archivo .cdf generado para crear el catálogo de seguridad para el ensamblado. Esta herramienta se incluye en CryptoAPI.
5.  Use la [utilidad SignTool](/windows/desktop/SecCrypto/signtool) para firmar el catálogo generado con el certificado usado en el paso 1. El archivo .cdf de los pasos 3 y 4 se puede eliminar una vez creado el catálogo.

Vea también Ejemplo [de firma de ensamblados](assembly-signing-example.md).

 

 
