---
title: Códigos de error de Win32 para ADSI
description: Los códigos de error de Win32 estándar también se usan para devolver mensajes de error ADSI.
ms.assetid: 5b7b85c9-ccca-4ea3-8b37-54f6b30a509f
ms.tgt_platform: multiple
keywords:
- Códigos de error de Win32 para ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a47151a3a1619a7f224dc0b9b7f0871813a346a3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103772883"
---
# <a name="win32-error-codes-for-adsi"></a><span data-ttu-id="6c0d2-104">Códigos de error de Win32 para ADSI</span><span class="sxs-lookup"><span data-stu-id="6c0d2-104">Win32 Error Codes for ADSI</span></span>

<span data-ttu-id="6c0d2-105">Los códigos de error de Win32 estándar también se usan para devolver mensajes de error ADSI.</span><span class="sxs-lookup"><span data-stu-id="6c0d2-105">Standard Win32 error codes are also used to return ADSI error messages.</span></span> <span data-ttu-id="6c0d2-106">En concreto, el proveedor LDAP de ADSI asigna todos los códigos de error LDAP a los códigos de error de Win32.</span><span class="sxs-lookup"><span data-stu-id="6c0d2-106">Specifically, the ADSI LDAP provider maps all the LDAP error codes to Win32 error codes.</span></span> <span data-ttu-id="6c0d2-107">Los valores **HRESULT** de estos códigos de error tienen el formato 0x8007XXXX, donde los últimos cuatro dígitos hexadecimales, xxxx, corresponden a los valores **DWORD** del código de error de Win32 adecuado.</span><span class="sxs-lookup"><span data-stu-id="6c0d2-107">The **HRESULT** values of these error codes are of the 0x8007XXXX format, where the last four hexadecimal digits, XXXX, corresponds to the **DWORD** values of the appropriate Win32 error code.</span></span> <span data-ttu-id="6c0d2-108">Por ejemplo, el valor de error de ADSI 0x80072020 proporciona el valor de error de Win32 de 0x2020 en formato hexadecimal o 8224 en formato decimal.</span><span class="sxs-lookup"><span data-stu-id="6c0d2-108">For example, the ADSI error value 0x80072020 gives the Win32 error value of 0x2020 in hexadecimal or 8224 in decimal.</span></span>

<span data-ttu-id="6c0d2-109">Para convertir el valor **HRESULT** de un código de error ADSI, devuelto por la aplicación, al valor **DWORD** del error de Win32 correspondiente, tal y como se define en los archivos de encabezado anteriores, utilice el procedimiento siguiente.</span><span class="sxs-lookup"><span data-stu-id="6c0d2-109">To convert the **HRESULT** value of an ADSI error code, returned by your application, to the corresponding the Win32 error **DWORD** value, as defined in the header files above, use the following procedure.</span></span>

<span data-ttu-id="6c0d2-110">La mayoría de los códigos de error de Win32 para ADSI se definen en Winerror. h o Lmerr. h.</span><span class="sxs-lookup"><span data-stu-id="6c0d2-110">Most of the Win32 error codes for ADSI are defined in Winerror.h or Lmerr.h.</span></span> <span data-ttu-id="6c0d2-111">Los valores de error se muestran como valores decimales en estos archivos.</span><span class="sxs-lookup"><span data-stu-id="6c0d2-111">The error values are listed as decimal values in these files.</span></span>

<span data-ttu-id="6c0d2-112">**Para convertir el valor **HRESULT** de un código de error ADSI en el correspondiente valor **DWORD** de error de Win32**</span><span class="sxs-lookup"><span data-stu-id="6c0d2-112">**To convert the **HRESULT** value of an ADSI error code to the corresponding the Win32 error **DWORD** value**</span></span>

1.  <span data-ttu-id="6c0d2-113">Convierta el valor **HRESULT** en un número hexadecimal si comienza con un valor decimal como puede obtener de una aplicación Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="6c0d2-113">Convert the **HRESULT** value to a hexadecimal number if starting with a decimal value as you may get from a Visual Basic application.</span></span>
2.  <span data-ttu-id="6c0d2-114">Quitar el elemento 0x8007 produce el resto.</span><span class="sxs-lookup"><span data-stu-id="6c0d2-114">Drop the 0x8007 part produce the remainder.</span></span>
3.  <span data-ttu-id="6c0d2-115">Convierta el resto en un número decimal.</span><span class="sxs-lookup"><span data-stu-id="6c0d2-115">Convert the remainder to a decimal number.</span></span>
4.  <span data-ttu-id="6c0d2-116">Buscar el resto decimal en Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="6c0d2-116">Look up the decimal remainder in Winerror.h.</span></span>
5.  <span data-ttu-id="6c0d2-117">Si no se encuentra en Winerror. h, reste 2100 del resto decimal y mire el resultado en Lmerr. h.</span><span class="sxs-lookup"><span data-stu-id="6c0d2-117">If not found in Winerror.h, subtract 2100 from the decimal remainder and look up the result in Lmerr.h.</span></span>

<span data-ttu-id="6c0d2-118">ADSI 2,0 asigna los códigos de error LDAP a un conjunto de códigos de error de Win32 que son diferentes de los que se usan en ADSI para Windows 2000 y el cliente DS.</span><span class="sxs-lookup"><span data-stu-id="6c0d2-118">ADSI 2.0 maps the LDAP error codes to a set of Win32 error codes that is different from that used in ADSI for Windows 2000 and DS Client.</span></span> <span data-ttu-id="6c0d2-119">Las diferencias se enumeran en:</span><span class="sxs-lookup"><span data-stu-id="6c0d2-119">The differences are listed in:</span></span>

-   [<span data-ttu-id="6c0d2-120">Códigos de error de Win32</span><span class="sxs-lookup"><span data-stu-id="6c0d2-120">Win32 Error Codes</span></span>](win32-error-codes.md)
-   [<span data-ttu-id="6c0d2-121">Códigos de error de Win32 para ADSI 2,0</span><span class="sxs-lookup"><span data-stu-id="6c0d2-121">Win32 Error Codes for ADSI 2.0</span></span>](win32-error-codes-for-adsi-2-0.md)

 

 




