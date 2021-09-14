---
description: Pktextract.exe es una herramienta que extrae el atributo publicKeyToken de un archivo de certificado.
ms.assetid: 195ff5bd-bb60-4053-9308-ceacd29853c0
title: Pktextract.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd163efabd01d65969788aefc2386b2f49079729
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071339"
---
# <a name="pktextractexe"></a>Pktextract.exe

Pktextract.exe es una herramienta que extrae el atributo **publicKeyToken** de un archivo de certificado. La salida es **publicKeyToken,** que es un identificador único de 16 caracteres (8 bytes) de la clave pública presente en el certificado, en un formato que se puede pegar fácilmente en una instrucción de identidad de ensamblado. El archivo de certificado debe estar presente en el mismo directorio que Pktextract.exe usar la utilidad . Pktextract.exe se proporciona en el Kit de desarrollo de software (SDK) de Microsoft Windows.

## <a name="syntax"></a>Sintaxis

**pktextract.exe** *<filename.cer>* **\[ -quiet \] \[ -nologo \]**

## <a name="command-line-options"></a>Opciones de la línea de comandos

Pktextract.exe usa las siguientes opciones de línea de comandos que no tienen en cuenta mayúsculas de minúsculas.



| Opción  | Descripción                                                          |
|---------|----------------------------------------------------------------------|
| -quiet  | Suprime la presentación completa de la información del certificado. Opcional.        |
| -nologo | Se ejecuta sin mostrar datos estándar de copyright de Microsoft. Opcional. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Herramientas de desarrollo de ensamblados en paralelo](side-by-side-assembly-development-tools.md)
</dt> </dl>

 

 



