---
title: '\_Solicitud de \_ Inicio de sesión \_ (Eaptypes. h) de EAP'
description: Almacena las credenciales de seguridad de EAP en una estructura de matriz de campos de entrada de configuración de EAP \_ \_ \_ \_ .
ms.assetid: 1F1A2F77-054D-4FD2-83A5-69C3D77418B3
keywords:
- EAP_CRED_LOGON_REQ
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2af29daa9d68e4cd2dd78f101585c2fa14d25200
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079140"
---
# <a name="eap_cred_logon_req"></a><span data-ttu-id="9465a-104">\_solicitud de \_ Inicio de sesión de recred de EAP \_</span><span class="sxs-lookup"><span data-stu-id="9465a-104">EAP\_CRED\_LOGON\_REQ</span></span>

<span data-ttu-id="9465a-105">La estructura de **solicitudes de inicio de sesión de EAP \_ \_ \_ CRED** almacena las credenciales de seguridad de EAP en una estructura de matriz de campos de entrada de [**\_ configuración \_ \_ \_ de EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array)</span><span class="sxs-lookup"><span data-stu-id="9465a-105">The **EAP\_CRED\_LOGON\_REQ** structure stores EAP security credentials within an [**EAP\_CONFIG\_INPUT\_FIELD\_ARRAY**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) structure.</span></span>


```C++
typedef EAP_CONFIG_INPUT_FIELD_ARRAY EAP_CRED_LOGON_REQ;
```



<dl> <dt>

<span data-ttu-id="9465a-106">**\_solicitud de \_ Inicio de sesión de recred de EAP \_**</span><span class="sxs-lookup"><span data-stu-id="9465a-106">**EAP\_CRED\_LOGON\_REQ**</span></span>
</dt> <dd>

<span data-ttu-id="9465a-107">La estructura de solicitudes de **\_ Inicio de \_ sesión \_ de EAP CRED** almacena las credenciales de seguridad de EAP a las que apunta el parámetro *pbUiData* de la estructura de [**\_ datos de interfaz de \_ usuario \_ interactiva de EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data) cuando el parámetro *dwDataType* del tipo de datos de [**\_ interfaz de usuario interactiva \_ \_ \_ de EAP**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_interactive_ui_data_type) especifica un tipo</span><span class="sxs-lookup"><span data-stu-id="9465a-107">The **EAP\_CRED\_LOGON\_REQ** structure stores EAP security credentials pointed to by the *pbUiData* parameter of the [**EAP\_INTERACTIVE\_UI\_DATA**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data) structure when the *dwDataType* parameter of [**EAP\_INTERACTIVE\_UI\_DATA\_TYPE**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_interactive_ui_data_type) specifies a credential request type.</span></span> <span data-ttu-id="9465a-108">Los campos de entrada de esta estructura son los mismos que los campos de entrada devueltos por [**EapHostPeerQueryCredentialInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerquerycredentialinputfields).</span><span class="sxs-lookup"><span data-stu-id="9465a-108">The input fields in this structure are the same as the input fields returned by [**EapHostPeerQueryCredentialInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerquerycredentialinputfields).</span></span> <span data-ttu-id="9465a-109">**EAP \_ de CRED \_ Logon \_ req** se usa en la solicitud de credenciales inicial y se usa la solicitud de reintento de [**EAP \_ \_**](eap-cred-req.md) en la solicitud de reintento de credencial durante una autenticación.</span><span class="sxs-lookup"><span data-stu-id="9465a-109">**EAP\_CRED\_LOGON\_REQ** is used in the initial credential request and [**EAP\_CRED\_REQ**](eap-cred-req.md) is used in the credential retry request during an authentication.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9465a-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9465a-110">Remarks</span></span>

<span data-ttu-id="9465a-111">La **estructura \_ \_ \_ req de inicio de sesión de EAP** se usa para admitir el inicio de sesión único (SSO).</span><span class="sxs-lookup"><span data-stu-id="9465a-111">The **EAP\_CRED\_LOGON\_REQ** structure is used to support Single-Sign-On (SSO).</span></span>

<span data-ttu-id="9465a-112">La estructura de **\_ req de inicio de \_ sesión \_ de EAP** es idéntica a la estructura de [**\_ \_ \_ resp de inicio**](eap-cred-logon-resp.md) de sesión de EAP.</span><span class="sxs-lookup"><span data-stu-id="9465a-112">The **EAP\_CRED\_LOGON\_REQ** structure is identical to the [**EAP\_CRED\_LOGON\_RESP**](eap-cred-logon-resp.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="9465a-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9465a-113">Requirements</span></span>



| <span data-ttu-id="9465a-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="9465a-114">Requirement</span></span> | <span data-ttu-id="9465a-115">Value</span><span class="sxs-lookup"><span data-stu-id="9465a-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9465a-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9465a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="9465a-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="9465a-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9465a-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9465a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="9465a-119">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="9465a-119">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="9465a-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9465a-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="9465a-121"><dt>Eaptypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="9465a-121"><dt>Eaptypes.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9465a-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="9465a-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9465a-123">**\_matriz de \_ campos de entrada de configuración de EAP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="9465a-123">**EAP\_CONFIG\_INPUT\_FIELD\_ARRAY**</span></span>](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array)
</dt> <dt>

[<span data-ttu-id="9465a-124">**\_solicitud de credenciales de EAP \_**</span><span class="sxs-lookup"><span data-stu-id="9465a-124">**EAP\_CRED\_REQ**</span></span>](eap-cred-req.md)
</dt> <dt>

[<span data-ttu-id="9465a-125">**\_datos de \_ interfaz de usuario interactiva de EAP \_**</span><span class="sxs-lookup"><span data-stu-id="9465a-125">**EAP\_INTERACTIVE\_UI\_DATA**</span></span>](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data)
</dt> <dt>

[<span data-ttu-id="9465a-126">**tipo de datos de interfaz de \_ usuario interactiva de EAP \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="9465a-126">**EAP\_INTERACTIVE\_UI\_DATA\_TYPE**</span></span>](/windows/desktop/api/eaptypes/ne-eaptypes-eap_interactive_ui_data_type)
</dt> <dt>

[<span data-ttu-id="9465a-127">**EapHostPeerQueryCredentialInputFields**</span><span class="sxs-lookup"><span data-stu-id="9465a-127">**EapHostPeerQueryCredentialInputFields**</span></span>](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerquerycredentialinputfields)
</dt> </dl>

 

 





