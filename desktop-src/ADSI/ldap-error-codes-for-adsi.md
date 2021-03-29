---
title: Códigos de error LDAP para ADSI
description: Cuando un servidor LDAP genera un error y pasa el error al cliente, el cliente LDAP traduce el error a una cadena.
ms.assetid: 7a0a5a1b-8473-405b-a590-3f917e50cbdc
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 149abf4562b0e35067149fb69c9a1ec1304cc528
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903044"
---
# <a name="ldap-error-codes-for-adsi"></a><span data-ttu-id="4ece6-103">Códigos de error LDAP para ADSI</span><span class="sxs-lookup"><span data-stu-id="4ece6-103">LDAP Error Codes for ADSI</span></span>

<span data-ttu-id="4ece6-104">Cuando un servidor LDAP genera un error y pasa el error al cliente, el cliente LDAP traduce el error a una cadena.</span><span class="sxs-lookup"><span data-stu-id="4ece6-104">When an LDAP server generates an error and passes the error to the client, the error is then translated into a string by the LDAP client.</span></span>

<span data-ttu-id="4ece6-105">Este método es similar a los [códigos de error de Win32 para ADSI](win32-error-codes-for-adsi.md).</span><span class="sxs-lookup"><span data-stu-id="4ece6-105">This method is similar to [Win32 error codes for ADSI](win32-error-codes-for-adsi.md).</span></span> <span data-ttu-id="4ece6-106">En este ejemplo, el código de error de cliente es el error 0x80072020 de WIN32.</span><span class="sxs-lookup"><span data-stu-id="4ece6-106">In this example, the client error code is the WIN32 error 0x80072020.</span></span>

<span data-ttu-id="4ece6-107">**Para determinar los códigos de error LDAP para ADSI**</span><span class="sxs-lookup"><span data-stu-id="4ece6-107">**To Determine the LDAP error codes for ADSI**</span></span>

1.  <span data-ttu-id="4ece6-108">Quite 8007 del código de error de WIN32.</span><span class="sxs-lookup"><span data-stu-id="4ece6-108">Drop the 8007 from the WIN32 error code.</span></span> <span data-ttu-id="4ece6-109">En el ejemplo, el valor hexadecimal restante es 2020.</span><span class="sxs-lookup"><span data-stu-id="4ece6-109">In the example, the remaining hex value is 2020.</span></span>
2.  <span data-ttu-id="4ece6-110">Convierta el valor hexadecimal restante en un valor decimal.</span><span class="sxs-lookup"><span data-stu-id="4ece6-110">Convert the remaining hex value to a decimal value.</span></span> <span data-ttu-id="4ece6-111">En el ejemplo, el valor hexadecimal restante 2020 se convierte en el valor decimal 8224.</span><span class="sxs-lookup"><span data-stu-id="4ece6-111">In the example, the remaining hex value 2020 converts to the decimal value 8224.</span></span>
3.  <span data-ttu-id="4ece6-112">Busque en el archivo WinError. h la definición del valor decimal.</span><span class="sxs-lookup"><span data-stu-id="4ece6-112">Search in the WinError.h file for the definition of the decimal value.</span></span> <span data-ttu-id="4ece6-113">En el ejemplo, 8224L corresponde al error de error de **\_ \_ las \_ operaciones de DS**.</span><span class="sxs-lookup"><span data-stu-id="4ece6-113">In the example, 8224L corresponds to the error **ERROR\_DS\_OPERATIONS\_ERROR**.</span></span>
4.  <span data-ttu-id="4ece6-114">Reemplace el prefijo **\_ DS de error** por **LDAP \_**.</span><span class="sxs-lookup"><span data-stu-id="4ece6-114">Replace the prefix **ERROR\_DS** with **LDAP\_**.</span></span> <span data-ttu-id="4ece6-115">En el ejemplo, la nueva definición es **\_ \_ error de operaciones LDAP**.</span><span class="sxs-lookup"><span data-stu-id="4ece6-115">In the example, the new definition is **LDAP\_OPERATIONS\_ERROR**.</span></span>
5.  <span data-ttu-id="4ece6-116">Busque el valor de la definición de error LDAP en el archivo Winldap. h.</span><span class="sxs-lookup"><span data-stu-id="4ece6-116">Search in the Winldap.h file for the value of the LDAP error definition.</span></span> <span data-ttu-id="4ece6-117">En el ejemplo, el valor de **\_ \_ error de operaciones LDAP** en el archivo Winldap. h es 0x01.</span><span class="sxs-lookup"><span data-stu-id="4ece6-117">In the example, the value of **LDAP\_OPERATIONS\_ERROR** in the Winldap.h file is 0x01.</span></span>

 

 




