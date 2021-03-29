---
description: Una aplicación puede utilizar la función RegSetValueEx para asociar un valor y sus datos con una clave. Para obtener una lista de los tipos de valor admitidos por RegSetValueEx, vea Registry Value Types.
ms.assetid: 75ac826a-f169-400c-b6d6-3e3ec9ebf996
title: Escribir y eliminar datos del registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5185c98f39a37512ec56fb994d5f1c4ba4b61ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360605"
---
# <a name="writing-and-deleting-registry-data"></a><span data-ttu-id="9c0a2-104">Escribir y eliminar datos del registro</span><span class="sxs-lookup"><span data-stu-id="9c0a2-104">Writing and Deleting Registry Data</span></span>

<span data-ttu-id="9c0a2-105">Una aplicación puede utilizar la función [**RegSetValueEx**](/windows/desktop/api/Winreg/nf-winreg-regsetvalueexa) para asociar un valor y sus datos con una clave.</span><span class="sxs-lookup"><span data-stu-id="9c0a2-105">An application can use the [**RegSetValueEx**](/windows/desktop/api/Winreg/nf-winreg-regsetvalueexa) function to associate a value and its data with a key.</span></span> <span data-ttu-id="9c0a2-106">Para obtener una lista de los tipos de valor admitidos por **RegSetValueEx**, vea [Registry Value Types](registry-value-types.md).</span><span class="sxs-lookup"><span data-stu-id="9c0a2-106">For a list of the value types supported by **RegSetValueEx**, see [Registry Value Types](registry-value-types.md).</span></span>

<span data-ttu-id="9c0a2-107">Para eliminar un valor de una clave, una aplicación puede usar la función [**error en regdeletevalue**](/windows/desktop/api/Winreg/nf-winreg-regdeletevaluea) .</span><span class="sxs-lookup"><span data-stu-id="9c0a2-107">To delete a value from a key, an application can use the [**RegDeleteValue**](/windows/desktop/api/Winreg/nf-winreg-regdeletevaluea) function.</span></span> <span data-ttu-id="9c0a2-108">Para eliminar una clave, puede usar la función [**RegDeleteKey**](/windows/desktop/api/Winreg/nf-winreg-regdeletekeya) .</span><span class="sxs-lookup"><span data-stu-id="9c0a2-108">To delete a key, it can use the [**RegDeleteKey**](/windows/desktop/api/Winreg/nf-winreg-regdeletekeya) function.</span></span> <span data-ttu-id="9c0a2-109">Una clave eliminada no se quita hasta que se cierra el último identificador de la misma.</span><span class="sxs-lookup"><span data-stu-id="9c0a2-109">A deleted key is not removed until the last handle to it has been closed.</span></span> <span data-ttu-id="9c0a2-110">No se pueden crear subclaves y valores bajo una clave eliminada.</span><span class="sxs-lookup"><span data-stu-id="9c0a2-110">Subkeys and values cannot be created under a deleted key.</span></span>

<span data-ttu-id="9c0a2-111">No es posible bloquear una clave del registro durante una operación de escritura para sincronizar el acceso a los datos.</span><span class="sxs-lookup"><span data-stu-id="9c0a2-111">It is not possible to lock a registry key during a write operation to synchronize access to the data.</span></span> <span data-ttu-id="9c0a2-112">Sin embargo, puede controlar el acceso a una clave del registro mediante atributos de seguridad.</span><span class="sxs-lookup"><span data-stu-id="9c0a2-112">However, you can control access to a registry key using security attributes.</span></span> <span data-ttu-id="9c0a2-113">Para obtener más información, consulte [seguridad y derechos de acceso de la clave del registro](registry-key-security-and-access-rights.md).</span><span class="sxs-lookup"><span data-stu-id="9c0a2-113">For more information, see [Registry Key Security and Access Rights](registry-key-security-and-access-rights.md).</span></span>

<span data-ttu-id="9c0a2-114">Se puede realizar más de una operación del registro dentro de una única transacción.</span><span class="sxs-lookup"><span data-stu-id="9c0a2-114">More than one registry operation can be performed within a single transaction.</span></span> <span data-ttu-id="9c0a2-115">Para asociar una clave del registro a una transacción, una aplicación puede usar la función [**RegCreateKeyTransacted**](/windows/desktop/api/Winreg/nf-winreg-regcreatekeytransacteda) o [**RegOpenKeyTransacted**](/windows/desktop/api/Winreg/nf-winreg-regopenkeytransacteda) .</span><span class="sxs-lookup"><span data-stu-id="9c0a2-115">To associate a registry key with a transaction, an application can use the [**RegCreateKeyTransacted**](/windows/desktop/api/Winreg/nf-winreg-regcreatekeytransacteda) or [**RegOpenKeyTransacted**](/windows/desktop/api/Winreg/nf-winreg-regopenkeytransacteda) function.</span></span> <span data-ttu-id="9c0a2-116">Para obtener más información acerca de las transacciones, consulte [Administrador de transacciones de kernel](/windows/desktop/Ktm/kernel-transaction-manager-portal).</span><span class="sxs-lookup"><span data-stu-id="9c0a2-116">For more information about transactions, see [Kernel Transaction Manager](/windows/desktop/Ktm/kernel-transaction-manager-portal).</span></span>

 

 
