---
description: Los proveedores de seguridad WMI se pueden usar para el scripting de WMI y para crear un proveedor de seguridad administrado.
ms.assetid: c3f7bd91-6cea-43ee-b8a7-1506dbd7926d
title: Proveedores de seguridad WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0206e337e5fa23470f015a0264bd77d53e8c4e14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666383"
---
# <a name="security-wmi-providers"></a><span data-ttu-id="78023-103">Proveedores de seguridad WMI</span><span class="sxs-lookup"><span data-stu-id="78023-103">Security WMI Providers</span></span>

## <a name="purpose"></a><span data-ttu-id="78023-104">Propósito</span><span class="sxs-lookup"><span data-stu-id="78023-104">Purpose</span></span>

<span data-ttu-id="78023-105">Los proveedores de seguridad de WMI permiten a los administradores y programadores configurar Cifrado de unidad BitLocker (BDE) y el Módulo de plataforma segura (TPM) mediante Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="78023-105">The Security WMI providers enable administrators and programmers to configure BitLocker Drive Encryption (BDE) and the Trusted Platform Module (TPM) using Windows Management Instrumentation (WMI).</span></span>

## <a name="developer-audience"></a><span data-ttu-id="78023-106">Audiencia de desarrolladores</span><span class="sxs-lookup"><span data-stu-id="78023-106">Developer audience</span></span>

<span data-ttu-id="78023-107">Este documento especifica la interfaz del proveedor WMI para administrar y configurar Cifrado de unidad BitLocker (BDE) y Módulo de plataforma segura (TPM) en Windows Server 2008 R2 y Windows Server 2008 para servidores, y Windows 7 y Windows Vista para equipos cliente.</span><span class="sxs-lookup"><span data-stu-id="78023-107">This document specifies the WMI provider interface for managing and configuring BitLocker Drive Encryption (BDE) and Trusted Platform Module (TPM) on Windows Server 2008 R2 and Windows Server 2008 for servers, and Windows 7 and Windows Vista for client computers.</span></span> <span data-ttu-id="78023-108">Está diseñado para ser leído por los scripts de escritura, los elementos de la interfaz de usuario u otras herramientas administrativas para BDE o TPM.</span><span class="sxs-lookup"><span data-stu-id="78023-108">It is intended to be read by those writing scripts, user interface elements, or other administrative tools for BDE or the TPM.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="78023-109">Requisitos de tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="78023-109">Run-time requirements</span></span>

<span data-ttu-id="78023-110">Los proveedores de WMI de seguridad requieren el archivo. mof especificado con cada proveedor y un sistema operativo compatible.</span><span class="sxs-lookup"><span data-stu-id="78023-110">The Security WMI Providers require the .mof file specified with each provider and a supported operating system.</span></span> <span data-ttu-id="78023-111">El sistema operativo mínimo es Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="78023-111">The minimum operating system is either Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="78023-112">Cifrado de unidad BitLocker solo está disponible para las versiones Windows Vista Enterprise y Windows Vista Ultimate de Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="78023-112">BitLocker Drive Encryption is only available for the Windows Vista Enterprise and Windows Vista Ultimate versions of Windows Vista.</span></span> <span data-ttu-id="78023-113">Para obtener información sobre los requisitos de tiempo de ejecución para un elemento de programación determinado, vea la sección de requisitos de la página de referencia de ese elemento.</span><span class="sxs-lookup"><span data-stu-id="78023-113">For information about run-time requirements for a particular programming element, see the Requirements section of the reference page for that element.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="78023-114">En esta sección</span><span class="sxs-lookup"><span data-stu-id="78023-114">In this section</span></span>



| <span data-ttu-id="78023-115">Tema</span><span class="sxs-lookup"><span data-stu-id="78023-115">Topic</span></span>                                                                               | <span data-ttu-id="78023-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="78023-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="78023-117">Acerca de los proveedores de WMI de seguridad</span><span class="sxs-lookup"><span data-stu-id="78023-117">About Security WMI Providers</span></span>](about-security-wmi-providers.md)<br/>         | <span data-ttu-id="78023-118">Breve introducción a los proveedores de WMI de seguridad.</span><span class="sxs-lookup"><span data-stu-id="78023-118">Brief overview of the Security WMI Providers.</span></span><br/>           |
| [<span data-ttu-id="78023-119">Referencia de proveedores de WMI de seguridad</span><span class="sxs-lookup"><span data-stu-id="78023-119">Security WMI Providers Reference</span></span>](security-wmi-providers-reference.md)<br/> | <span data-ttu-id="78023-120">Documentación de referencia de los proveedores de WMI de seguridad.</span><span class="sxs-lookup"><span data-stu-id="78023-120">Reference documentation for the Security WMI Providers.</span></span><br/> |



 

## <a name="additional-resources"></a><span data-ttu-id="78023-121">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="78023-121">Additional resources</span></span>

<span data-ttu-id="78023-122">Los siguientes son recursos adicionales.</span><span class="sxs-lookup"><span data-stu-id="78023-122">The following are additional resources.</span></span>



|                    |                                                                                                                                                                        |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78023-123">Clases</span><span class="sxs-lookup"><span data-stu-id="78023-123">Classes</span></span><br/> | <span data-ttu-id="78023-124">Para obtener más información acerca de los proveedores de WMI de seguridad, vea [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) y [**Win32 \_ TPM**](win32-tpm.md).</span><span class="sxs-lookup"><span data-stu-id="78023-124">For more information about the Security WMI providers, see [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) and [**Win32\_Tpm**](win32-tpm.md).</span></span><br/> |



 

 

 




