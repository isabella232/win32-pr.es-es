---
title: Cadenas de estilo C
description: Una aplicación WinSNMP puede usar cadenas de estilo C terminadas en NULL para convertir objetos de entidad y de identificador de objeto (OID) a y desde sus representaciones de cadena.
ms.assetid: df04071c-df46-410b-ad92-6adecbfcd454
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 878398b6d8691982aa90b9f1376a38214030e52e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903009"
---
# <a name="c-style-strings"></a><span data-ttu-id="42791-103">Cadenas de estilo C</span><span class="sxs-lookup"><span data-stu-id="42791-103">C-Style Strings</span></span>

<span data-ttu-id="42791-104">Una aplicación WinSNMP puede usar cadenas de estilo C terminadas en **null** para convertir objetos de entidad y de identificador de objeto (OID) a y desde sus representaciones de cadena.</span><span class="sxs-lookup"><span data-stu-id="42791-104">A WinSNMP application can use **NULL**-terminated C-style strings to convert entity and object identifier (OID) objects to and from their string representations.</span></span>

<span data-ttu-id="42791-105">Entre las funciones WinSNMP que manipulan cadenas de estilo C se incluyen [**SnmpStrToEntity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtoentity), [**SnmpEntityToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpentitytostr), [**SnmpStrToOid**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtooid)y [**SnmpOidToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidtostr).</span><span class="sxs-lookup"><span data-stu-id="42791-105">The WinSNMP functions that manipulate C-style strings include [**SnmpStrToEntity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtoentity), [**SnmpEntityToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpentitytostr), [**SnmpStrToOid**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtooid), and [**SnmpOidToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidtostr).</span></span> <span data-ttu-id="42791-106">Dado que [**SnmpEntityToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpentitytostr) y [**SnmpOidToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidtostr) devuelven un puntero a una variable de cadena de estilo C, la aplicación WinSNMP debe pasar un valor adecuado en el parámetro *size* cuando realiza llamadas a estas funciones.</span><span class="sxs-lookup"><span data-stu-id="42791-106">Because [**SnmpEntityToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpentitytostr) and [**SnmpOidToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidtostr) return a pointer to a C-style string variable, the WinSNMP application must pass an appropriate value in the *size* parameter when it makes calls to these functions.</span></span> <span data-ttu-id="42791-107">Para obtener más información, vea las páginas de referencia de estas funciones.</span><span class="sxs-lookup"><span data-stu-id="42791-107">For more information, see the reference pages for these functions.</span></span>

> [!Note]  
> <span data-ttu-id="42791-108">El parámetro de *contexto* de las funciones [**SnmpStrToContext**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtocontext) y [**SnmpContextToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcontexttostr) debe ser una estructura de cadena de octetos, es decir, una estructura [**smiOCTETS**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) .</span><span class="sxs-lookup"><span data-stu-id="42791-108">The *context* parameter of the [**SnmpStrToContext**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtocontext) and [**SnmpContextToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcontexttostr) functions must be an octet string structure, that is, an [**smiOCTETS**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) structure.</span></span> <span data-ttu-id="42791-109">El parámetro de *contexto* no puede ser una cadena de estilo C.</span><span class="sxs-lookup"><span data-stu-id="42791-109">The *context* parameter cannot be a C-style string.</span></span> <span data-ttu-id="42791-110">La cadena contenida en una estructura **smiOCTETS** no requiere un byte de terminación **null**.</span><span class="sxs-lookup"><span data-stu-id="42791-110">The string contained in an **smiOCTETS** structure does not require a **NULL**-terminating byte.</span></span>

 

 

 




