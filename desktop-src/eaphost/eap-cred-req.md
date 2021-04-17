---
title: '\_Solicitud de credenciales de EAP \_ (Eaptypes. h)'
description: Almacena las credenciales de seguridad de EAP en una estructura de matriz de campos de entrada de configuración de EAP \_ \_ \_ \_ . | \_Solicitud de credenciales de EAP \_ (Eaptypes. h)
ms.assetid: 537a90fc-4dd2-44d4-93da-949f31130ac4
keywords:
- EAP_CRED_REQ
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20da4e6aa8b1ab24dfd9cd791236d1f9b26304f6
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105698119"
---
# <a name="eap_cred_req"></a><span data-ttu-id="af5fa-105">\_solicitud de credenciales de EAP \_</span><span class="sxs-lookup"><span data-stu-id="af5fa-105">EAP\_CRED\_REQ</span></span>

<span data-ttu-id="af5fa-106">La **estructura \_ \_ req req de EAP** almacena las credenciales de seguridad de EAP dentro de una estructura de matriz de [**campos de entrada de configuración de EAP \_ \_ \_ \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) .</span><span class="sxs-lookup"><span data-stu-id="af5fa-106">The **EAP\_CRED\_REQ** structure stores EAP security credentials within a [**EAP\_CONFIG\_INPUT\_FIELD\_ARRAY**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) structure.</span></span>


```C++
typedef EAP_CONFIG_INPUT_FIELD_ARRAY EAP_CRED_REQ;
```



<dl> <dt>

<span data-ttu-id="af5fa-107">**\_solicitud de credenciales de EAP \_**</span><span class="sxs-lookup"><span data-stu-id="af5fa-107">**EAP\_CRED\_REQ**</span></span>
</dt> <dd>

<span data-ttu-id="af5fa-108">La **estructura \_ \_ req req de EAP** almacena las credenciales de seguridad de EAP antiguas y nuevas a las que apunta el parámetro *pbUiData* de la estructura de datos de [**\_ interfaz de \_ usuario \_ interactiva de EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data) cuando el parámetro *DwDataType* del tipo de [**datos de interfaz de \_ usuario interactiva \_ \_ \_ de EAP**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_interactive_ui_data_type) especifica un tipo de solicitud de credenciales.</span><span class="sxs-lookup"><span data-stu-id="af5fa-108">The **EAP\_CRED\_REQ** structure stores both the old and new EAP security credentials pointed to by the *pbUiData* parameter of the [**EAP\_INTERACTIVE\_UI\_DATA**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data) structure when the *dwDataType* parameter of [**EAP\_INTERACTIVE\_UI\_DATA\_TYPE**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_interactive_ui_data_type) specifies a credential request type.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="af5fa-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="af5fa-109">Remarks</span></span>

<span data-ttu-id="af5fa-110">La estructura de **\_ \_ solicitud de credenciales de EAP** se usa para admitir el inicio de sesión único (SSO).</span><span class="sxs-lookup"><span data-stu-id="af5fa-110">The **EAP\_CRED\_REQ** structure is used to support Single-Sign-On (SSO).</span></span>

<span data-ttu-id="af5fa-111">La estructura de REQ de la **\_ \_ solicitud EAP** es idéntica a la estructura de [**\_ \_ resp de EAP**](eap-cred-resp.md) .</span><span class="sxs-lookup"><span data-stu-id="af5fa-111">The **EAP\_CRED\_REQ** structure is identical to the [**EAP\_CRED\_RESP**](eap-cred-resp.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="af5fa-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="af5fa-112">Requirements</span></span>



| <span data-ttu-id="af5fa-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="af5fa-113">Requirement</span></span> | <span data-ttu-id="af5fa-114">Value</span><span class="sxs-lookup"><span data-stu-id="af5fa-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="af5fa-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="af5fa-115">Minimum supported client</span></span><br/> | <span data-ttu-id="af5fa-116">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="af5fa-116">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="af5fa-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="af5fa-117">Minimum supported server</span></span><br/> | <span data-ttu-id="af5fa-118">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="af5fa-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="af5fa-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="af5fa-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="af5fa-120"><dt>Eaptypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="af5fa-120"><dt>Eaptypes.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="af5fa-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="af5fa-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af5fa-122">Estructuras de suplicante de EAPHost</span><span class="sxs-lookup"><span data-stu-id="af5fa-122">EAPHost Supplicant Structures</span></span>](eap-host-supplicant-structures.md)
</dt> <dt>

[<span data-ttu-id="af5fa-123">**respuesta de cred de EAP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="af5fa-123">**EAP\_CRED\_RESP**</span></span>](eap-cred-resp.md)
</dt> <dt>

[<span data-ttu-id="af5fa-124">**\_solicitud de \_ expiración de credenciales de EAP \_**</span><span class="sxs-lookup"><span data-stu-id="af5fa-124">**EAP\_CRED\_EXPIRY\_REQ**</span></span>](/windows/desktop/api/eaptypes/ns-eaptypes-eap_cred_expiry_req)
</dt> <dt>

<span data-ttu-id="af5fa-125">[**respuesta \_ de \_ expiración de credenciales de EAP \_**](/previous-versions/windows/desktop/legacy/bb530539(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="af5fa-125">[**EAP\_CRED\_EXPIRY\_RESP**](/previous-versions/windows/desktop/legacy/bb530539(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="af5fa-126">**\_datos de \_ interfaz de usuario interactiva de EAP \_**</span><span class="sxs-lookup"><span data-stu-id="af5fa-126">**EAP\_INTERACTIVE\_UI\_DATA**</span></span>](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data)
</dt> <dt>

[<span data-ttu-id="af5fa-127">SSO y PLAP</span><span class="sxs-lookup"><span data-stu-id="af5fa-127">SSO and PLAP</span></span>](understanding-sso-and-plap.md)
</dt> </dl>

 

