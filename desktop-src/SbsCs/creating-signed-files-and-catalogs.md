---
description: Para firmar un archivo y crear un catálogo para él, primero debe tener un proceso para firmar archivos, un certificado y una clave pública.
ms.assetid: 61337ea6-2d6b-4080-9128-5b8527512ce6
title: Crear archivos y catálogos firmados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df1327ed2d64c6f7be9f14acc2c846cf8a887119
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127271652"
---
# <a name="creating-signed-files-and-catalogs"></a>Crear archivos y catálogos firmados

Para firmar un archivo y crear un catálogo para él, primero debe tener un proceso para firmar archivos, un certificado y una clave pública.

**Para firmar un archivo y crear un catálogo**

1.  Use [Pktextract.exe](pktextract-exe.md) para extraer el [*token de clave pública*](p-sbscs-gly.md) del archivo de certificado. El archivo de certificado debe estar presente en el mismo directorio que la utilidad .
2.  Use el valor del token de clave pública para actualizar el **atributo publicKeyToken** del **elemento assemblyIdentity** en el archivo de manifiesto.
3.  Use [MT.exe](mt-exe.md) para generar hashes de archivos contenidos en el manifiesto del ensamblado y para crear el archivo de descripción del catálogo (.cdf).
4.  Use Makecat.exe con el archivo .cdf generado para crear el catálogo de seguridad para el ensamblado. Esta herramienta se incluye en CryptoAPI.
5.  Use la [utilidad SignTool](/windows/desktop/SecCrypto/signtool) para firmar el catálogo generado con el certificado usado en el paso 1. El archivo .cdf de los pasos 3 y 4 se puede eliminar una vez creado el catálogo.

Vea también Ejemplo [de firma de ensamblado.](assembly-signing-example.md)

 

 
