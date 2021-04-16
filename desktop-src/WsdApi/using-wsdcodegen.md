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
# <a name="using-wsdcodegen"></a><span data-ttu-id="d4fcb-103">Usar WsdCodeGen</span><span class="sxs-lookup"><span data-stu-id="d4fcb-103">Using WsdCodeGen</span></span>

<span data-ttu-id="d4fcb-104">**Para compilar una aplicación WSDAPI mediante WsdCodeGen**</span><span class="sxs-lookup"><span data-stu-id="d4fcb-104">**To build a WSDAPI application using WsdCodeGen**</span></span>

1.  <span data-ttu-id="d4fcb-105">Defina el contrato funcional para el host del dispositivo en un archivo WSDL.</span><span class="sxs-lookup"><span data-stu-id="d4fcb-105">Define the functional contract for the device host in a WSDL file.</span></span>
2.  <span data-ttu-id="d4fcb-106">Genere un archivo de configuración mediante WsdCodeGen.</span><span class="sxs-lookup"><span data-stu-id="d4fcb-106">Generate a configuration file using WsdCodeGen.</span></span> <span data-ttu-id="d4fcb-107">Para obtener más información, consulte [archivo de configuración de WsdCodeGen](wsdcodegen-configuration-file.md) y sintaxis de la línea de comandos de [WsdCodeGen](wsdcodegen-command-line-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="d4fcb-107">For more information, see [WsdCodeGen Configuration File](wsdcodegen-configuration-file.md) and [WsdCodeGen Command Line Syntax](wsdcodegen-command-line-syntax.md).</span></span>
3.  <span data-ttu-id="d4fcb-108">Abra el archivo de configuración generado y modifique el archivo como sea necesario.</span><span class="sxs-lookup"><span data-stu-id="d4fcb-108">Open the generated configuration file and modify the file as required.</span></span> <span data-ttu-id="d4fcb-109">Si va a compilar una aplicación cliente, es necesario realizar una pequeña o ninguna modificación.</span><span class="sxs-lookup"><span data-stu-id="d4fcb-109">If you are building a client application, little or no modification is required.</span></span> <span data-ttu-id="d4fcb-110">Si va a compilar una aplicación host, cambie los elementos de configuración específicos del usuario (por ejemplo, [**fabricante**](manufacturer.md) y [**modelName**](modelname.md)).</span><span class="sxs-lookup"><span data-stu-id="d4fcb-110">If you are building a host application, change the user-specific configuration elements (such as [**manufacturer**](manufacturer.md) and [**modelName**](modelname.md)).</span></span>
4.  <span data-ttu-id="d4fcb-111">Genere código mediante WsdCodeGen y proporcione el archivo de configuración como entrada.</span><span class="sxs-lookup"><span data-stu-id="d4fcb-111">Generate code using WsdCodeGen, providing the configuration file as input.</span></span> <span data-ttu-id="d4fcb-112">Para obtener más información, consulte sintaxis de la [línea de comandos de WsdCodeGen](wsdcodegen-command-line-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="d4fcb-112">For more information, see [WsdCodeGen Command Line Syntax](wsdcodegen-command-line-syntax.md).</span></span>
5.  <span data-ttu-id="d4fcb-113">Use el código generado para compilar un cliente, un host o ambos.</span><span class="sxs-lookup"><span data-stu-id="d4fcb-113">Use the generated code to build a client, host, or both.</span></span>

<span data-ttu-id="d4fcb-114">El Windows SDK incluye algunos archivos WSDL de ejemplo, archivos de configuración de WsdCodeGen y código generado.</span><span class="sxs-lookup"><span data-stu-id="d4fcb-114">The Windows SDK includes some sample WSDL files, WsdCodeGen configuration files, and generated code.</span></span> <span data-ttu-id="d4fcb-115">Para obtener más información, vea [ejemplos de WSDAPI](wsdapi-samples.md).</span><span class="sxs-lookup"><span data-stu-id="d4fcb-115">For more information, see [WSDAPI Samples](wsdapi-samples.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d4fcb-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d4fcb-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d4fcb-117">Ejemplos de WSDAPI</span><span class="sxs-lookup"><span data-stu-id="d4fcb-117">WSDAPI Samples</span></span>](wsdapi-samples.md)
</dt> </dl>

 

 



