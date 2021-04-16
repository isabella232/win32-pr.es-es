---
description: Describe el proceso de creación de una aplicación de WSDAPI mediante WsdCodeGen.
ms.assetid: 8f172e2c-4cd1-4108-9c8d-01a731aca83b
title: Usar WsdCodeGen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e09bd2b0c8f96d51751aa90bc3206a0824f19b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706379"
---
# <a name="using-wsdcodegen"></a>Usar WsdCodeGen

**Para compilar una aplicación WSDAPI mediante WsdCodeGen**

1.  Defina el contrato funcional para el host del dispositivo en un archivo WSDL.
2.  Genere un archivo de configuración mediante WsdCodeGen. Para obtener más información, consulte [archivo de configuración de WsdCodeGen](wsdcodegen-configuration-file.md) y sintaxis de la línea de comandos de [WsdCodeGen](wsdcodegen-command-line-syntax.md).
3.  Abra el archivo de configuración generado y modifique el archivo como sea necesario. Si va a compilar una aplicación cliente, es necesario realizar una pequeña o ninguna modificación. Si va a compilar una aplicación host, cambie los elementos de configuración específicos del usuario (por ejemplo, [**fabricante**](manufacturer.md) y [**modelName**](modelname.md)).
4.  Genere código mediante WsdCodeGen y proporcione el archivo de configuración como entrada. Para obtener más información, consulte sintaxis de la [línea de comandos de WsdCodeGen](wsdcodegen-command-line-syntax.md).
5.  Use el código generado para compilar un cliente, un host o ambos.

El Windows SDK incluye algunos archivos WSDL de ejemplo, archivos de configuración de WsdCodeGen y código generado. Para obtener más información, vea [ejemplos de WSDAPI](wsdapi-samples.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ejemplos de WSDAPI](wsdapi-samples.md)
</dt> </dl>

 

 



