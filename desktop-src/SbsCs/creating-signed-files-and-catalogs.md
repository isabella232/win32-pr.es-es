---
description: Para firmar un archivo y crear un catálogo para él, primero debe tener un proceso para firmar archivos, un certificado y una clave pública.
ms.assetid: 61337ea6-2d6b-4080-9128-5b8527512ce6
title: Crear archivos y catálogos firmados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df1327ed2d64c6f7be9f14acc2c846cf8a887119
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277150"
---
# <a name="creating-signed-files-and-catalogs"></a>Crear archivos y catálogos firmados

Para firmar un archivo y crear un catálogo para él, primero debe tener un proceso para firmar archivos, un certificado y una clave pública.

**Para firmar un archivo y crear un catálogo**

1.  Use [Pktextract.exe](pktextract-exe.md) para extraer el [*token de clave pública*](p-sbscs-gly.md) del archivo de certificado. El archivo de certificado debe estar presente en el mismo directorio que la utilidad.
2.  Use el valor del token de clave pública para actualizar el atributo **PublicKeyToken** del elemento **assemblyIdentity** en el archivo de manifiesto.
3.  Utilice [MT.exe](mt-exe.md) para generar valores hash de los archivos contenidos en el manifiesto del ensamblado y para crear el archivo de Descripción del catálogo (. CDF).
4.  Use Makecat.exe con el. CDF generado para crear el catálogo de seguridad para el ensamblado. Esta herramienta se incluye en la CryptoAPI.
5.  Use la utilidad [SignTool](/windows/desktop/SecCrypto/signtool) para firmar el catálogo generado con el certificado usado en el paso 1. El. CDF de los pasos 3 y 4 se puede eliminar una vez que se crea el catálogo.

Vea también el [ejemplo de firma de ensamblados](assembly-signing-example.md).

 

 
