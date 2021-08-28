---
description: Describe el proceso de creación de una aplicación WSDAPI mediante WsdCodeGen.
ms.assetid: 8f172e2c-4cd1-4108-9c8d-01a731aca83b
title: Uso de WsdCodeGen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6395d39a84415cc56e66949ea82ef7a1acd9fc009b7e1b2c93fa2712e8a81a9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119463175"
---
# <a name="using-wsdcodegen"></a>Uso de WsdCodeGen

**Para compilar una aplicación WSDAPI mediante WsdCodeGen**

1.  Defina el contrato funcional para el host de dispositivo en un archivo WSDL.
2.  Genere un archivo de configuración mediante WsdCodeGen. Para obtener más información, vea Archivo de configuración [WsdCodeGen](wsdcodegen-configuration-file.md) y Sintaxis de la línea de comandos [de WsdCodeGen.](wsdcodegen-command-line-syntax.md)
3.  Abra el archivo de configuración generado y modifique el archivo según sea necesario. Si va a compilar una aplicación cliente, se requiere poca o ninguna modificación. Si va a compilar una aplicación host, cambie los elementos de configuración específicos del usuario (por [**ejemplo, manufacturer**](manufacturer.md) y [**modelName).**](modelname.md)
4.  Genere código mediante WsdCodeGen, proporcionando el archivo de configuración como entrada. Para obtener más información, vea Sintaxis de la línea de comandos de [WsdCodeGen.](wsdcodegen-command-line-syntax.md)
5.  Use el código generado para compilar un cliente, un host o ambos.

El SDK Windows incluye algunos archivos WSDL de ejemplo, archivos de configuración WsdCodeGen y código generado. Para obtener más información, vea [Ejemplos de WSDAPI.](wsdapi-samples.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ejemplos de WSDAPI](wsdapi-samples.md)
</dt> </dl>

 

 



