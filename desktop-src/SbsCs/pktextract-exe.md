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
# <a name="pktextractexe"></a><span data-ttu-id="c8d65-103">Pktextract.exe</span><span class="sxs-lookup"><span data-stu-id="c8d65-103">Pktextract.exe</span></span>

<span data-ttu-id="c8d65-104">Pktextract.exe es una herramienta que extrae el atributo **PublicKeyToken** de un archivo de certificado.</span><span class="sxs-lookup"><span data-stu-id="c8d65-104">Pktextract.exe is a tool that extracts the **publicKeyToken** attribute from a certificate file.</span></span> <span data-ttu-id="c8d65-105">El resultado es el **PublicKeyToken**, que es un identificador único de 16 caracteres (8 bytes) de la clave pública presente en el certificado, en un formato que se puede pegar fácilmente en una instrucción de identidad de ensamblado.</span><span class="sxs-lookup"><span data-stu-id="c8d65-105">The output is the **publicKeyToken**, which is a unique 16-character (8-byte) identifier of the public key present in the certificate, in a format that can easily be pasted into an assembly identity statement.</span></span> <span data-ttu-id="c8d65-106">El archivo de certificado debe estar presente en el mismo directorio que Pktextract.exe para usar la utilidad.</span><span class="sxs-lookup"><span data-stu-id="c8d65-106">The certificate file must be present in the same directory as Pktextract.exe to use the utility.</span></span> <span data-ttu-id="c8d65-107">Pktextract.exe se proporciona en el kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="c8d65-107">Pktextract.exe is provided in the Microsoft Windows Software Development Kit (SDK).</span></span>

## <a name="syntax"></a><span data-ttu-id="c8d65-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c8d65-108">Syntax</span></span>

<span data-ttu-id="c8d65-109">**pktextract.exe** *<FILENAME. cer>* **\[ -Quiet \] \[ -nologo \]**</span><span class="sxs-lookup"><span data-stu-id="c8d65-109">**pktextract.exe** *<filename.cer>* **\[-quiet\] \[-nologo\]**</span></span>

## <a name="command-line-options"></a><span data-ttu-id="c8d65-110">Opciones de la línea de comandos</span><span class="sxs-lookup"><span data-stu-id="c8d65-110">Command Line Options</span></span>

<span data-ttu-id="c8d65-111">Pktextract.exe usa las siguientes opciones de la línea de comandos que no distinguen mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="c8d65-111">Pktextract.exe uses the following case-insensitive command line options.</span></span>



| <span data-ttu-id="c8d65-112">Opción</span><span class="sxs-lookup"><span data-stu-id="c8d65-112">Option</span></span>  | <span data-ttu-id="c8d65-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="c8d65-113">Description</span></span>                                                          |
|---------|----------------------------------------------------------------------|
| <span data-ttu-id="c8d65-114">-quiet</span><span class="sxs-lookup"><span data-stu-id="c8d65-114">-quiet</span></span>  | <span data-ttu-id="c8d65-115">Suprime la presentación completa de la información del certificado.</span><span class="sxs-lookup"><span data-stu-id="c8d65-115">Suppresses full display of certificate information.</span></span> <span data-ttu-id="c8d65-116">Opcional.</span><span class="sxs-lookup"><span data-stu-id="c8d65-116">Optional.</span></span>        |
| <span data-ttu-id="c8d65-117">-nologo</span><span class="sxs-lookup"><span data-stu-id="c8d65-117">-nologo</span></span> | <span data-ttu-id="c8d65-118">Se ejecuta sin mostrar los datos de copyright de Microsoft estándar.</span><span class="sxs-lookup"><span data-stu-id="c8d65-118">Runs without displaying standard Microsoft copyright data.</span></span> <span data-ttu-id="c8d65-119">Opcional.</span><span class="sxs-lookup"><span data-stu-id="c8d65-119">Optional.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="c8d65-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c8d65-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c8d65-121">Herramientas de desarrollo de ensamblados en paralelo</span><span class="sxs-lookup"><span data-stu-id="c8d65-121">Side-by-Side Assembly Development Tools</span></span>](side-by-side-assembly-development-tools.md)
</dt> </dl>

 

 



