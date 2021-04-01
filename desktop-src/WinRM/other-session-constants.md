---
title: Otras constantes de sesión (WSManDisp. h)
description: Especifique la codificación, el cifrado y el puerto de nombre de entidad de seguridad de servicio.
ms.assetid: a921b7bc-1f40-427c-971f-c0bc9c9f6887
ms.tgt_platform: multiple
topic_type:
- apiref
api_name:
- WSManFlagUTF8
- WSManFlagNoEncryption
- WSManFlagEnableSPNServerPort
- WSManFlagUTF16
api_location:
- WSManDisp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 236e69d80db2ad30b8cc2934b6b2016d7eecbed6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150936"
---
# <a name="other-session-constants"></a><span data-ttu-id="48807-103">Otras constantes de sesión</span><span class="sxs-lookup"><span data-stu-id="48807-103">Other Session Constants</span></span>

<span data-ttu-id="48807-104">Constantes, enumeradas en la lista siguiente, en la enumeración **\_ \_ WSManSessionFlags** que especifican la codificación, el cifrado y el puerto de nombre de entidad de seguridad de servicio.</span><span class="sxs-lookup"><span data-stu-id="48807-104">Constants, listed in the following list, in the **\_\_WSManSessionFlags** enumeration that specify encoding, encryption, and service principal name port.</span></span>

<dl> <dt>

<span data-ttu-id="48807-105"><span id="WSManFlagUTF8"></span><span id="wsmanflagutf8"></span><span id="WSMANFLAGUTF8"></span>**WSManFlagUTF8**</span><span class="sxs-lookup"><span data-stu-id="48807-105"><span id="WSManFlagUTF8"></span><span id="wsmanflagutf8"></span><span id="WSMANFLAGUTF8"></span>**WSManFlagUTF8**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48807-106">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="48807-106">1 (0x1)</span></span>
</dt> <dt>



<span data-ttu-id="48807-107">Envía la solicitud en UTF8 en lugar de UTF16.</span><span class="sxs-lookup"><span data-stu-id="48807-107">Sends the request in UTF8 rather than UTF16.</span></span>

<span data-ttu-id="48807-108">El método de scripting asociado es [**WSMan. SessionFlagUTF8**](wsman-sessionflagutf8.md) y el método de C++ es [**IWSManEx. SessionFlagUTF8**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagutf8).</span><span class="sxs-lookup"><span data-stu-id="48807-108">The associated scripting method is [**WSMan.SessionFlagUTF8**](wsman-sessionflagutf8.md) and the C++ method is [**IWSManEx.SessionFlagUTF8**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagutf8).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48807-109"><span id="WSManFlagNoEncryption"></span><span id="wsmanflagnoencryption"></span><span id="WSMANFLAGNOENCRYPTION"></span>**WSManFlagNoEncryption**</span><span class="sxs-lookup"><span data-stu-id="48807-109"><span id="WSManFlagNoEncryption"></span><span id="wsmanflagnoencryption"></span><span id="WSMANFLAGNOENCRYPTION"></span>**WSManFlagNoEncryption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48807-110">1048576 (0x100000)</span><span class="sxs-lookup"><span data-stu-id="48807-110">1048576 (0x100000)</span></span>
</dt> <dt>



<span data-ttu-id="48807-111">No Cifre los mensajes enviados a través de la red.</span><span class="sxs-lookup"><span data-stu-id="48807-111">Do not encrypt the messages sent over the network.</span></span> <span data-ttu-id="48807-112">Esta configuración solo se permite si el [*agente de escucha*](windows-remote-management-glossary.md) está configurado de modo que **AllowUnencrypted** esté establecido en **true**.</span><span class="sxs-lookup"><span data-stu-id="48807-112">This setting is allowed only if the [*listener*](windows-remote-management-glossary.md) is configured so that **AllowUnencrypted** is set to **True**.</span></span>

<span data-ttu-id="48807-113">El método de scripting asociado es [**WSMan. SessionFlagNoEncryption**](wsman-sessionflagnoencryption.md) y el método de C++ es [**IWSManEx. SessionFlagNoEncryption**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagnoencryption).</span><span class="sxs-lookup"><span data-stu-id="48807-113">The associated scripting method is [**WSMan.SessionFlagNoEncryption**](wsman-sessionflagnoencryption.md) and the C++ method is [**IWSManEx.SessionFlagNoEncryption**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagnoencryption).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48807-114"><span id="WSManFlagEnableSPNServerPort"></span><span id="wsmanflagenablespnserverport"></span><span id="WSMANFLAGENABLESPNSERVERPORT"></span>**WSManFlagEnableSPNServerPort**</span><span class="sxs-lookup"><span data-stu-id="48807-114"><span id="WSManFlagEnableSPNServerPort"></span><span id="wsmanflagenablespnserverport"></span><span id="WSMANFLAGENABLESPNSERVERPORT"></span>**WSManFlagEnableSPNServerPort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48807-115">4194304 (0x400000)</span><span class="sxs-lookup"><span data-stu-id="48807-115">4194304 (0x400000)</span></span>
</dt> <dt>



<span data-ttu-id="48807-116">Especifique el puerto de nombre de entidad de seguridad de servicio (SPN) al conectarse directamente al hardware de BMC remoto, también conocido como conexión [*fuera de banda*](windows-remote-management-glossary.md) .</span><span class="sxs-lookup"><span data-stu-id="48807-116">Specify the Service Principal Name (SPN) port when connecting directly to remote BMC hardware, also known as an [*out-of-band*](windows-remote-management-glossary.md) connection.</span></span> <span data-ttu-id="48807-117">Dado que el equipo servidor WinRM y el hardware de BMC pueden compartir la misma dirección IP, esta marca indica que se debe usar el número de puerto de SPN para determinar si la conexión es al servicio o directamente al BMC.</span><span class="sxs-lookup"><span data-stu-id="48807-117">Because both the WinRM server computer and the BMC hardware can share the same IP address, this flag indicates that the SPN port number must be used to determine whether the connection is to the service or directly to the BMC.</span></span> <span data-ttu-id="48807-118">Para obtener más información, vea [formatos de nombre para SPN únicos](/windows/desktop/AD/name-formats-for-unique-spns).</span><span class="sxs-lookup"><span data-stu-id="48807-118">For more information, see [Name Formats for Unique SPNs](/windows/desktop/AD/name-formats-for-unique-spns).</span></span>

<span data-ttu-id="48807-119">El método de scripting asociado es [**WSMan. SessionFlagEnableSPNServerPort**](wsman-sessionflagenablespnserverport.md) y el método de C++ es [**IWSManEx. SessionFlagEnableSPNServerPort**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagenablespnserverport).</span><span class="sxs-lookup"><span data-stu-id="48807-119">The associated scripting method is [**WSMan.SessionFlagEnableSPNServerPort**](wsman-sessionflagenablespnserverport.md) and the C++ method is [**IWSManEx.SessionFlagEnableSPNServerPort**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagenablespnserverport).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48807-120"><span id="WSManFlagUTF16"></span><span id="wsmanflagutf16"></span><span id="WSMANFLAGUTF16"></span>**WSManFlagUTF16**</span><span class="sxs-lookup"><span data-stu-id="48807-120"><span id="WSManFlagUTF16"></span><span id="wsmanflagutf16"></span><span id="WSMANFLAGUTF16"></span>**WSManFlagUTF16**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48807-121">0x800000</span><span class="sxs-lookup"><span data-stu-id="48807-121">0x800000</span></span>
</dt> <dt>



<span data-ttu-id="48807-122">Envía la solicitud en UTF16.</span><span class="sxs-lookup"><span data-stu-id="48807-122">Sends the request in UTF16.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="48807-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="48807-123">Requirements</span></span>



| <span data-ttu-id="48807-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="48807-124">Requirement</span></span> | <span data-ttu-id="48807-125">Value</span><span class="sxs-lookup"><span data-stu-id="48807-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="48807-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="48807-126">Minimum supported client</span></span><br/> | <span data-ttu-id="48807-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="48807-127">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="48807-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="48807-128">Minimum supported server</span></span><br/> | <span data-ttu-id="48807-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="48807-129">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="48807-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="48807-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="48807-131"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="48807-131"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="48807-132">IDL</span><span class="sxs-lookup"><span data-stu-id="48807-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="48807-133"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="48807-133"><dt>WSManDisp.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="48807-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="48807-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48807-135">Constantes de sesión</span><span class="sxs-lookup"><span data-stu-id="48807-135">Session Constants</span></span>](session-constants.md)
</dt> </dl>

 

