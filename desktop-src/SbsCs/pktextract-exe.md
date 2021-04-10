---
description: Pktextract.exe es una herramienta que extrae el atributo publicKeyToken de un archivo de certificado.
ms.assetid: 195ff5bd-bb60-4053-9308-ceacd29853c0
title: Pktextract.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd163efabd01d65969788aefc2386b2f49079729
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156148"
---
# <a name="pktextractexe"></a>Pktextract.exe

Pktextract.exe es una herramienta que extrae el atributo **PublicKeyToken** de un archivo de certificado. El resultado es el **PublicKeyToken**, que es un identificador único de 16 caracteres (8 bytes) de la clave pública presente en el certificado, en un formato que se puede pegar fácilmente en una instrucción de identidad de ensamblado. El archivo de certificado debe estar presente en el mismo directorio que Pktextract.exe para usar la utilidad. Pktextract.exe se proporciona en el kit de desarrollo de software (SDK) de Microsoft Windows.

## <a name="syntax"></a>Sintaxis

**pktextract.exe** *<FILENAME. cer>* **\[ -Quiet \] \[ -nologo \]**

## <a name="command-line-options"></a>Opciones de la línea de comandos

Pktextract.exe usa las siguientes opciones de la línea de comandos que no distinguen mayúsculas de minúsculas.



| Opción  | Descripción                                                          |
|---------|----------------------------------------------------------------------|
| -quiet  | Suprime la presentación completa de la información del certificado. Opcional.        |
| -nologo | Se ejecuta sin mostrar los datos de copyright de Microsoft estándar. Opcional. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Herramientas de desarrollo de ensamblados en paralelo](side-by-side-assembly-development-tools.md)
</dt> </dl>

 

 



