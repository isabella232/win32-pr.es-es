---
description: Obtiene los parámetros de configuración de EAPOL para la interfaz LAN inalámbrica especificada.
ms.assetid: 3dce15be-879d-42e9-b8eb-96d52c004acb
title: Función WZCEapolGetInterfaceParams (wzcsapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WZCEapolGetInterfaceParams
api_type:
- DllExport
api_location:
- Wzcsapi.dll
ms.openlocfilehash: bc89fd2defb75662fa90b5ed00c7969d483da590
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678302"
---
# <a name="wzceapolgetinterfaceparams-function"></a><span data-ttu-id="dadf4-103">WZCEapolGetInterfaceParams función)</span><span class="sxs-lookup"><span data-stu-id="dadf4-103">WZCEapolGetInterfaceParams function</span></span>

<span data-ttu-id="dadf4-104">\[**WZCEapolGetInterfaceParams** ya no es compatible con Windows Vista y windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="dadf4-104">\[**WZCEapolGetInterfaceParams** is no longer supported as of Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="dadf4-105">En su lugar, use la [API WiFi nativa](native-wifi-reference.md), que proporciona una funcionalidad similar.</span><span class="sxs-lookup"><span data-stu-id="dadf4-105">Instead, use the [Native Wifi API](native-wifi-reference.md), which provides similar functionality.</span></span> <span data-ttu-id="dadf4-106">Para obtener más información, consulte [acerca de la API WiFi nativa](about-the-native-wifi-api.md).\]</span><span class="sxs-lookup"><span data-stu-id="dadf4-106">For more information, see [About the Native Wifi API](about-the-native-wifi-api.md).\]</span></span>

<span data-ttu-id="dadf4-107">La función **WZCEapolGetInterfaceParams** obtiene los parámetros de configuración de EAPOL para la interfaz LAN inalámbrica especificada.</span><span class="sxs-lookup"><span data-stu-id="dadf4-107">The **WZCEapolGetInterfaceParams** function gets EAPOL configuration parameters for the specified wireless LAN interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="dadf4-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dadf4-108">Syntax</span></span>


```C++
DWORD WZCEapolGetInterfaceParams(
  _In_    LPWSTR            pSrvAddr,
  _In_    PWCHAR            pwszGuid,
  _In_    DWORD             dwSizeOfSSID,
  _In_    BYTE              *pbSSID,
  _Inout_ EAPOL_INTF_PARAMS *pIntfParams
);
```



## <a name="parameters"></a><span data-ttu-id="dadf4-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dadf4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dadf4-110">*pSrvAddr* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="dadf4-110">*pSrvAddr* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dadf4-111">Puntero a una cadena que contiene el nombre del equipo en el que se va a ejecutar esta función.</span><span class="sxs-lookup"><span data-stu-id="dadf4-111">A pointer to a string containing the name of the computer on which to execute this function.</span></span> <span data-ttu-id="dadf4-112">Si este parámetro es **null**, se llama al servicio de configuración inalámbrica cero en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="dadf4-112">If this parameter is **NULL**, then the Wireless Zero Configuration service is called on the local computer.</span></span>

<span data-ttu-id="dadf4-113">Si el parámetro *pSrvAddr* especificado es un equipo remoto, el equipo remoto debe admitir llamadas RPC remotas.</span><span class="sxs-lookup"><span data-stu-id="dadf4-113">If the *pSrvAddr* parameter specified is a remote computer, then the remote computer must support remote RPC calls.</span></span>

</dd> <dt>

<span data-ttu-id="dadf4-114">*pwszGuid* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="dadf4-114">*pwszGuid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dadf4-115">GUID de la interfaz para la que se van a recuperar los datos.</span><span class="sxs-lookup"><span data-stu-id="dadf4-115">The GUID of the interface for which data is to be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="dadf4-116">*dwSizeOfSSID* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="dadf4-116">*dwSizeOfSSID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dadf4-117">Tamaño del identificador de red para el que se van a recuperar los datos.</span><span class="sxs-lookup"><span data-stu-id="dadf4-117">The size of the network identifier for which data is to be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="dadf4-118">*pbSSID* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="dadf4-118">*pbSSID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dadf4-119">Puntero al identificador de red para el que se van a recuperar los datos.</span><span class="sxs-lookup"><span data-stu-id="dadf4-119">A pointer to the network identifier for which data is to be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="dadf4-120">*pIntfParams* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="dadf4-120">*pIntfParams* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="dadf4-121">Un puntero a una estructura de parámetros [**\_ \_ Intf de EAPOL**](eapol-intf-params.md) que contiene parámetros de interfaz.</span><span class="sxs-lookup"><span data-stu-id="dadf4-121">A pointer to a [**EAPOL\_INTF\_PARAMS**](eapol-intf-params.md) structure that contains interface parameters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dadf4-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dadf4-122">Return value</span></span>

<span data-ttu-id="dadf4-123">Devuelve \_ un error si la operación se completa correctamente; de lo contrario, devuelve uno de los códigos de error del sistema de Windows.</span><span class="sxs-lookup"><span data-stu-id="dadf4-123">Returns ERROR\_SUCCESS if the operation completes successfully; otherwise, returns one of the Windows system error codes.</span></span>

## <a name="remarks"></a><span data-ttu-id="dadf4-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dadf4-124">Remarks</span></span>

<span data-ttu-id="dadf4-125">Si **WZCEapolGetInterfaceParams** devuelve un error \_ , el llamador debe llamar a [**LocalFree**](/windows/win32/api/winbase/nf-winbase-localfree) para liberar los búferes internos asignados para los datos devueltos cuando ya no se necesite esta información.</span><span class="sxs-lookup"><span data-stu-id="dadf4-125">If the **WZCEapolGetInterfaceParams** returns ERROR\_SUCCESS, the caller should call [**LocalFree**](/windows/win32/api/winbase/nf-winbase-localfree) to release the internal buffers allocated for the data returned once this information is no longer needed.</span></span>

> [!Note]  
> <span data-ttu-id="dadf4-126">El archivo de encabezado *wzcsapi. h* y el archivo de biblioteca de importación *wzcsapi. lib* no están disponibles en el Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="dadf4-126">The *Wzcsapi.h* header file and *Wzcsapi.lib* import library file are not available in the Windows SDK.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="dadf4-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dadf4-127">Requirements</span></span>



| <span data-ttu-id="dadf4-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="dadf4-128">Requirement</span></span> | <span data-ttu-id="dadf4-129">Value</span><span class="sxs-lookup"><span data-stu-id="dadf4-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="dadf4-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dadf4-130">Minimum supported client</span></span><br/> | <span data-ttu-id="dadf4-131">Solo aplicaciones de escritorio de Windows XP con SP2 \[\]</span><span class="sxs-lookup"><span data-stu-id="dadf4-131">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="dadf4-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dadf4-132">Minimum supported server</span></span><br/> | <span data-ttu-id="dadf4-133">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="dadf4-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="dadf4-134">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="dadf4-134">End of client support</span></span><br/>    | <span data-ttu-id="dadf4-135">Windows XP con SP3</span><span class="sxs-lookup"><span data-stu-id="dadf4-135">Windows XP with SP3</span></span><br/>                                                         |
| <span data-ttu-id="dadf4-136">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="dadf4-136">End of server support</span></span><br/>    | <span data-ttu-id="dadf4-137">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="dadf4-137">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="dadf4-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="dadf4-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="dadf4-139"><dt>Wzcsapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="dadf4-139"><dt>Wzcsapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="dadf4-140">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="dadf4-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="dadf4-141"><dt>Wzcsapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dadf4-141"><dt>Wzcsapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="dadf4-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="dadf4-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dadf4-143"><dt>Wzcsapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dadf4-143"><dt>Wzcsapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dadf4-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="dadf4-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dadf4-145">**WZCEnumInterfaces**</span><span class="sxs-lookup"><span data-stu-id="dadf4-145">**WZCEnumInterfaces**</span></span>](wzcenuminterfaces.md)
</dt> <dt>

[<span data-ttu-id="dadf4-146">**WZCQueryInterface**</span><span class="sxs-lookup"><span data-stu-id="dadf4-146">**WZCQueryInterface**</span></span>](wzcqueryinterface.md)
</dt> <dt>

[<span data-ttu-id="dadf4-147">**WZCRefreshInterface**</span><span class="sxs-lookup"><span data-stu-id="dadf4-147">**WZCRefreshInterface**</span></span>](wzcrefreshinterface.md)
</dt> </dl>

 

 
