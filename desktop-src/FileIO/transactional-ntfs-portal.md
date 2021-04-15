---
description: NTFS transaccional (TxF) permite realizar operaciones de archivo en un volumen del sistema de archivos NTFS en una transacción.
ms.assetid: e8c3ceed-d391-4934-b3f7-12c2123c8c23
title: NTFS transaccional (TxF)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7553bfc7cae0b5389762527f0ac726c674a6a03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539926"
---
# <a name="transactional-ntfs-txf"></a><span data-ttu-id="b5642-103">NTFS transaccional (TxF)</span><span class="sxs-lookup"><span data-stu-id="b5642-103">Transactional NTFS (TxF)</span></span>

<span data-ttu-id="b5642-104">\[Microsoft recomienda encarecidamente que los desarrolladores usen medios alternativos para lograr las necesidades de las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="b5642-104">\[Microsoft strongly recommends developers utilize alternative means to achieve your application s needs.</span></span> <span data-ttu-id="b5642-105">Muchos escenarios para los que se desarrolló TxF se pueden lograr mediante técnicas más sencillas y más fáciles de usar.</span><span class="sxs-lookup"><span data-stu-id="b5642-105">Many scenarios that TxF was developed for can be achieved through simpler and more readily available techniques.</span></span> <span data-ttu-id="b5642-106">Además, es posible que TxF no esté disponible en versiones futuras de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="b5642-106">Furthermore, TxF may not be available in future versions of Microsoft Windows.</span></span> <span data-ttu-id="b5642-107">Para obtener más información y alternativas a TxF, vea [alternativas al uso de NTFS transaccional](deprecation-of-txf.md).\]</span><span class="sxs-lookup"><span data-stu-id="b5642-107">For more information, and alternatives to TxF, please see [Alternatives to using Transactional NTFS](deprecation-of-txf.md).\]</span></span>

## <a name="purpose"></a><span data-ttu-id="b5642-108">Propósito</span><span class="sxs-lookup"><span data-stu-id="b5642-108">Purpose</span></span>

<span data-ttu-id="b5642-109">NTFS transaccional (TxF) permite realizar operaciones de archivo en un volumen del sistema de archivos NTFS en una transacción.</span><span class="sxs-lookup"><span data-stu-id="b5642-109">Transactional NTFS (TxF) allows file operations on an NTFS file system volume to be performed in a transaction.</span></span> <span data-ttu-id="b5642-110">Las transacciones de TxF aumentan la confiabilidad de la aplicación al proteger la integridad de los datos en los errores y simplificar el desarrollo de aplicaciones al reducir considerablemente la cantidad de código de control de errores.</span><span class="sxs-lookup"><span data-stu-id="b5642-110">TxF transactions increase application reliability by protecting data integrity across failures and simplify application development by greatly reducing the amount of error handling code.</span></span>

<span data-ttu-id="b5642-111">TxF usa el marco de trabajo de transacciones proporcionado por el [Administrador de transacciones de kernel](/windows/desktop/Ktm/kernel-transaction-manager-portal) (KTM).</span><span class="sxs-lookup"><span data-stu-id="b5642-111">TxF uses the transaction framework provided by the [Kernel Transaction Manager](/windows/desktop/Ktm/kernel-transaction-manager-portal) (KTM).</span></span> <span data-ttu-id="b5642-112">Esto permite que las operaciones de archivo TxF formen parte de una transacción que implique otros orígenes de datos, como SQL Server y el registro de transacciones (TxR).</span><span class="sxs-lookup"><span data-stu-id="b5642-112">This allows TxF file operations to be part of a transaction involving other data sources such as SQL Server and Transacted Registry (TxR).</span></span>

## <a name="where-applicable"></a><span data-ttu-id="b5642-113">Donde sea aplicable</span><span class="sxs-lookup"><span data-stu-id="b5642-113">Where applicable</span></span>

<span data-ttu-id="b5642-114">Una aplicación puede usar TxF para conservar la integridad de los datos en el disco causados por condiciones de error inesperadas y ayudar a resolver escenarios de usuario del sistema de archivos simultáneos aislando los cambios de otros mientras se realizan los cambios.</span><span class="sxs-lookup"><span data-stu-id="b5642-114">An application can use TxF to preserve the integrity of data on disk caused by unexpected error conditions and help resolve concurrent file-system user scenarios by isolating your changes from others while the changes are being made.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="b5642-115">Audiencia de desarrolladores</span><span class="sxs-lookup"><span data-stu-id="b5642-115">Developer audience</span></span>

<span data-ttu-id="b5642-116">Antes de usar TxF, debe tener conocimientos prácticos de las transacciones mediante KTM o [Coordinador de transacciones distribuidas (DTC)](/previous-versions/windows/desktop/ms684146(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b5642-116">Before using TxF, you should have a working knowledge of transactions using either KTM or [Distributed Transaction Coordinator (DTC)](/previous-versions/windows/desktop/ms684146(v=vs.85)).</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="b5642-117">Requisitos de tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="b5642-117">Run-time requirements</span></span>

<span data-ttu-id="b5642-118">TxF está disponible a partir de Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="b5642-118">TxF is available starting with Windows Vista.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="b5642-119">En esta sección</span><span class="sxs-lookup"><span data-stu-id="b5642-119">In this section</span></span>



| <span data-ttu-id="b5642-120">Tema</span><span class="sxs-lookup"><span data-stu-id="b5642-120">Topic</span></span>                                                    | <span data-ttu-id="b5642-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="b5642-121">Description</span></span>                                                                                                |
|----------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b5642-122">Acerca de</span><span class="sxs-lookup"><span data-stu-id="b5642-122">About</span></span>](about-transactional-ntfs.md)<br/>         | <span data-ttu-id="b5642-123">Información general acerca de NTFS transaccional.</span><span class="sxs-lookup"><span data-stu-id="b5642-123">General information about Transactional NTFS.</span></span><br/>                                                   |
| [<span data-ttu-id="b5642-124">Referencia</span><span class="sxs-lookup"><span data-stu-id="b5642-124">Reference</span></span>](transactional-ntfs-reference.md)<br/> | <span data-ttu-id="b5642-125">Documentación para las funciones, estructuras de datos, enumeraciones y otros elementos de programación.</span><span class="sxs-lookup"><span data-stu-id="b5642-125">Documentation for the functions, data structures, enumerations, and other programming elements.</span></span><br/> |



 

 

