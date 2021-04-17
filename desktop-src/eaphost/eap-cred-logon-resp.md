---
title: EAP \_ CRED \_ Logon \_ Resp (Eaptypes. h)
description: Almacena las credenciales de seguridad de EAP en una estructura de matriz de campos de entrada de configuración de EAP \_ \_ \_ \_ . | EAP \_ CRED \_ Logon \_ Resp (Eaptypes. h)
ms.assetid: 1244A40F-6999-4053-97C4-1C4FB107B2F5
keywords:
- EAP_CRED_LOGON_RESP
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0e1bbabc30918efaed0e286b5df231537ed5543
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105698120"
---
# <a name="eap_cred_logon_resp"></a><span data-ttu-id="e625b-105">EAP de inicio de sesión de la \_ \_ \_ resp</span><span class="sxs-lookup"><span data-stu-id="e625b-105">EAP\_CRED\_LOGON\_RESP</span></span>

<span data-ttu-id="e625b-106">La estructura de **\_ resp de inicio de \_ \_ sesión de EAP** almacena las credenciales de seguridad de EAP en una estructura de [**\_ \_ \_ \_ matriz de campos de entrada de configuración de EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) .</span><span class="sxs-lookup"><span data-stu-id="e625b-106">The **EAP\_CRED\_LOGON\_RESP** structure stores EAP security credentials within a [**EAP\_CONFIG\_INPUT\_FIELD\_ARRAY**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) structure.</span></span>


```C++
typedef EAP_CONFIG_INPUT_FIELD_ARRAY EAP_CRED_LOGON_RESP;
```



<dl> <dt>

<span data-ttu-id="e625b-107">**EAP de inicio de sesión de la \_ \_ \_ resp**</span><span class="sxs-lookup"><span data-stu-id="e625b-107">**EAP\_CRED\_LOGON\_RESP**</span></span>
</dt> <dd>

<span data-ttu-id="e625b-108">La estructura de **resp de \_ Inicio de \_ sesión \_ de EAP** almacena las credenciales de seguridad de EAP a las que apunta el parámetro *pbUiData* de la estructura de datos de [**\_ interfaz de \_ usuario \_ interactiva de EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data) cuando el parámetro *dwDataType* del [**\_ \_ \_ \_ tipo de datos Interactive UI de EAP**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_interactive_ui_data_type) especifica un tipo de solicitud de credencial</span><span class="sxs-lookup"><span data-stu-id="e625b-108">The **EAP\_CRED\_LOGON\_RESP** structure stores EAP security credentials pointed to by the *pbUiData* parameter of the [**EAP\_INTERACTIVE\_UI\_DATA**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data) structure when the *dwDataType* parameter of [**EAP\_INTERACTIVE\_UI\_DATA\_TYPE**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_interactive_ui_data_type) specifies a credential request type.</span></span> <span data-ttu-id="e625b-109">Los campos de entrada de esta estructura serán los mismos que los campos de entrada devueltos por [**EapHostPeerQueryCredentialInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerquerycredentialinputfields).</span><span class="sxs-lookup"><span data-stu-id="e625b-109">The input fields in this structure will be same as the input fields returned by [**EapHostPeerQueryCredentialInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerquerycredentialinputfields).</span></span> <span data-ttu-id="e625b-110">**EAP \_ de CRED \_ Logon \_ resp** se usa en la solicitud de credenciales inicial y [**EAP \_ CRED \_ resp**](eap-cred-resp.md) se usa en la solicitud de reintento de credencial durante una autenticación.</span><span class="sxs-lookup"><span data-stu-id="e625b-110">**EAP\_CRED\_LOGON\_RESP** is used in the initial credential request and [**EAP\_CRED\_RESP**](eap-cred-resp.md) is used in the credential retry request during an authentication.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e625b-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e625b-111">Remarks</span></span>

<span data-ttu-id="e625b-112">La estructura de uso de **\_ credenciales de \_ Inicio de sesión \_ de EAP** se usa para admitir el inicio de sesión único (SSO).</span><span class="sxs-lookup"><span data-stu-id="e625b-112">The **EAP\_CRED\_LOGON\_RESP** structure is used to support Single-Sign-On (SSO).</span></span>

<span data-ttu-id="e625b-113">La estructura de **\_ resp de inicio de \_ \_ sesión de EAP** es idéntica a la estructura [**\_ \_ \_ req del inicio de sesión de EAP**](eap-cred-logon-req.md) .</span><span class="sxs-lookup"><span data-stu-id="e625b-113">The **EAP\_CRED\_LOGON\_RESP** structure is identical to the [**EAP\_CRED\_LOGON\_REQ**](eap-cred-logon-req.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="e625b-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e625b-114">Requirements</span></span>



| <span data-ttu-id="e625b-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="e625b-115">Requirement</span></span> | <span data-ttu-id="e625b-116">Value</span><span class="sxs-lookup"><span data-stu-id="e625b-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e625b-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e625b-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e625b-118">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="e625b-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e625b-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e625b-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e625b-120">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="e625b-120">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="e625b-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e625b-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="e625b-122"><dt>Eaptypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="e625b-122"><dt>Eaptypes.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e625b-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="e625b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e625b-124">**EapHostPeerQueryCredentialInputFields**</span><span class="sxs-lookup"><span data-stu-id="e625b-124">**EapHostPeerQueryCredentialInputFields**</span></span>](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerquerycredentialinputfields)
</dt> <dt>

[<span data-ttu-id="e625b-125">**\_matriz de \_ campos de entrada de configuración de EAP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e625b-125">**EAP\_CONFIG\_INPUT\_FIELD\_ARRAY**</span></span>](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array)
</dt> <dt>

[<span data-ttu-id="e625b-126">**\_solicitud de \_ Inicio de sesión de recred de EAP \_**</span><span class="sxs-lookup"><span data-stu-id="e625b-126">**EAP\_CRED\_LOGON\_REQ**</span></span>](eap-cred-logon-req.md)
</dt> <dt>

[<span data-ttu-id="e625b-127">**\_datos de \_ interfaz de usuario interactiva de EAP \_**</span><span class="sxs-lookup"><span data-stu-id="e625b-127">**EAP\_INTERACTIVE\_UI\_DATA**</span></span>](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data)
</dt> <dt>

[<span data-ttu-id="e625b-128">**tipo de datos de interfaz de \_ usuario interactiva de EAP \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e625b-128">**EAP\_INTERACTIVE\_UI\_DATA\_TYPE**</span></span>](/windows/desktop/api/eaptypes/ne-eaptypes-eap_interactive_ui_data_type)
</dt> </dl>

 

 





