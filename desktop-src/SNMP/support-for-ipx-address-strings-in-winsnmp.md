---
title: Compatibilidad con cadenas de direcciones IPX en WinSNMP
description: WinSNMP 2,0 formaliza el uso de cadenas de direcciones IPX.
ms.assetid: b90b8e95-dab0-483b-9336-07e20c122cba
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc33c3ff3b589f9614b139260cef993e232f4343
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103772847"
---
# <a name="support-for-ipx-address-strings-in-winsnmp"></a><span data-ttu-id="7ed44-103">Compatibilidad con cadenas de direcciones IPX en WinSNMP</span><span class="sxs-lookup"><span data-stu-id="7ed44-103">Support for IPX Address Strings in WinSNMP</span></span>

<span data-ttu-id="7ed44-104">WinSNMP 2,0 formaliza el uso de cadenas de direcciones IPX.</span><span class="sxs-lookup"><span data-stu-id="7ed44-104">WinSNMP 2.0 formalizes the use of IPX address strings.</span></span> <span data-ttu-id="7ed44-105">Si especifica una cadena de dirección IPX como parámetro de entrada para la función [**SnmpStrToEntity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtoentity) , debe dar formato a la cadena mediante los siguientes estándares:</span><span class="sxs-lookup"><span data-stu-id="7ed44-105">If you specify an IPX address string as an input parameter to the [**SnmpStrToEntity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtoentity) function, you must format the string using the following standards:</span></span>

-   <span data-ttu-id="7ed44-106">Un número de red que consta de ocho dígitos hexadecimales (relleno de cero si es necesario).</span><span class="sxs-lookup"><span data-stu-id="7ed44-106">A network number that consists of eight hexadecimal digits (zero-filled if necessary)</span></span>
-   <span data-ttu-id="7ed44-107">Un separador (":", "." o "–")</span><span class="sxs-lookup"><span data-stu-id="7ed44-107">A separator (either ":", "." or " – ")</span></span>
-   <span data-ttu-id="7ed44-108">Un número de nodo que consta de 12 dígitos hexadecimales (relleno de cero si es necesario).</span><span class="sxs-lookup"><span data-stu-id="7ed44-108">A node number that consists of 12 hexadecimal digits (zero-filled if necessary)</span></span>

<span data-ttu-id="7ed44-109">Por ejemplo, 00000001:00081A0D01C2 o 00000001.00081 a0d01c2.</span><span class="sxs-lookup"><span data-stu-id="7ed44-109">For example, 00000001:00081A0D01C2 or 00000001.00081a0d01c2.</span></span> <span data-ttu-id="7ed44-110">Los dígitos hexadecimales pueden estar en mayúsculas o minúsculas.</span><span class="sxs-lookup"><span data-stu-id="7ed44-110">Hexadecimal digits can be uppercase or lowercase.</span></span>

<span data-ttu-id="7ed44-111">Este es el formato que usa la función [**SnmpEntityToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpentitytostr) para devolver una cadena de dirección IPX.</span><span class="sxs-lookup"><span data-stu-id="7ed44-111">This is the format the [**SnmpEntityToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpentitytostr) function uses to return an IPX address string.</span></span> <span data-ttu-id="7ed44-112">La cadena se devuelve cuando una aplicación que funciona en uno de los modos sin \_ traducir snmpapi llama a la función **SnmpEntityToStr** .</span><span class="sxs-lookup"><span data-stu-id="7ed44-112">The string is returned when an application that is operating in one of the SNMPAPI\_UNTRANSLATED modes calls the **SnmpEntityToStr** function.</span></span> <span data-ttu-id="7ed44-113">También se puede devolver la cadena cuando la aplicación funciona en el \_ modo traducido de snmpapi y no hay ningún nombre descriptivo disponible para la entidad.</span><span class="sxs-lookup"><span data-stu-id="7ed44-113">The string can also be returned when the application is operating in SNMPAPI\_TRANSLATED mode and no user-friendly name is available for the entity.</span></span>

 

 




