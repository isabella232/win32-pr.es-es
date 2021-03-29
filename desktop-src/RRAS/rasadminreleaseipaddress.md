---
title: Función de devolución de llamada RasAdminReleaseIpAddress
description: La función RasAdminReleaseIpAddress es una función definida por la aplicación que se exporta mediante un archivo DLL de administración de servidor RAS de terceros.
ms.assetid: 86fd9173-f158-4de5-8166-483a652a52cc
keywords:
- Función de devolución de llamada RasAdminReleaseIpAddress RAS
topic_type:
- apiref
api_name:
- RasAdminReleaseIpAddress
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d58c162ebc6d340b9bd913407bc00aac87e208e4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793510"
---
# <a name="rasadminreleaseipaddress-callback-function"></a><span data-ttu-id="2df2c-104">Función de devolución de llamada RasAdminReleaseIpAddress</span><span class="sxs-lookup"><span data-stu-id="2df2c-104">RasAdminReleaseIpAddress callback function</span></span>

<span data-ttu-id="2df2c-105">\[La función **RasAdminReleaseIpAddress** está disponible para su uso en Windows NT 4,0 y no está disponible en las versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="2df2c-105">\[The **RasAdminReleaseIpAddress** function is available for use in Windows NT 4.0 and is unavailable in subsequent versions.</span></span> <span data-ttu-id="2df2c-106">En su lugar, use [**MprAdminReleaseIpAddress**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminreleaseipaddress).\]</span><span class="sxs-lookup"><span data-stu-id="2df2c-106">Instead, use [**MprAdminReleaseIpAddress**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminreleaseipaddress).\]</span></span>

<span data-ttu-id="2df2c-107">La función **RasAdminReleaseIpAddress** es una función definida por la aplicación que se exporta mediante un archivo dll de administración de servidor RAS de terceros.</span><span class="sxs-lookup"><span data-stu-id="2df2c-107">The **RasAdminReleaseIpAddress** function is an application-defined function that is exported by a third-party RAS server administration DLL.</span></span> <span data-ttu-id="2df2c-108">RAS llama a esta función para notificar a la DLL que el cliente remoto se desconectó y que se debe liberar la dirección IP.</span><span class="sxs-lookup"><span data-stu-id="2df2c-108">RAS calls this function to notify the DLL that the remote client was disconnected and that the IP address should be released.</span></span>

## <a name="syntax"></a><span data-ttu-id="2df2c-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2df2c-109">Syntax</span></span>


```C++
void CALLBACK RasAdminReleaseIpAddress(
  _In_ WCHAR  *lpszUserName,
  _In_ WCHAR  *lpszPortName,
  _In_ IPADDR *pipAddress
);
```



## <a name="parameters"></a><span data-ttu-id="2df2c-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2df2c-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2df2c-111">*lpszUserName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2df2c-111">*lpszUserName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2df2c-112">Especifica el puntero a una cadena Unicode terminada en null que especifica el nombre de un usuario remoto para el que se obtuvo previamente una dirección IP mediante la función [**RasAdminGetIpAddressForUser**](rasadmingetipaddressforuser.md) .</span><span class="sxs-lookup"><span data-stu-id="2df2c-112">Specifies the pointer to a null-terminated Unicode string that specifies the name of a remote user for whom an IP address was previously obtained using the [**RasAdminGetIpAddressForUser**](rasadmingetipaddressforuser.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="2df2c-113">*lpszPortName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2df2c-113">*lpszPortName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2df2c-114">Puntero a una cadena Unicode terminada en null que especifica el nombre del puerto en el que está conectado el usuario especificado por *lpszUserName* .</span><span class="sxs-lookup"><span data-stu-id="2df2c-114">Pointer to a null-terminated Unicode string that specifies the name of the port on which the user specified by *lpszUserName* is connected.</span></span>

</dd> <dt>

<span data-ttu-id="2df2c-115">*pipAddress* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2df2c-115">*pipAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2df2c-116">Puntero a una variable **DirIP** que especifica la dirección IP devuelta para este usuario en una llamada anterior a [**RasAdminGetIpAddressForUser**](rasadmingetipaddressforuser.md).</span><span class="sxs-lookup"><span data-stu-id="2df2c-116">Pointer to an **IPADDR** variable that specifies the IP address returned for this user in a previous call to [**RasAdminGetIpAddressForUser**](rasadmingetipaddressforuser.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2df2c-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2df2c-117">Return value</span></span>

<span data-ttu-id="2df2c-118">No hay información de error extendida para esta función; no llame a [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="2df2c-118">There is no extended error information for this function; do no call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="2df2c-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2df2c-119">Remarks</span></span>

<span data-ttu-id="2df2c-120">El servidor RAS llama a la función **RasAdminReleaseIpAddress** solo si la aplicación devolvió **true** en el parámetro *bNotifyRelease* durante la llamada anterior a [**RasAdminGetIpAddressForUser**](rasadmingetipaddressforuser.md) para el usuario especificado por el parámetro *lpszUserName* .</span><span class="sxs-lookup"><span data-stu-id="2df2c-120">The RAS server calls the **RasAdminReleaseIpAddress** function only if the application returned **TRUE** in the *bNotifyRelease* parameter during the earlier call to [**RasAdminGetIpAddressForUser**](rasadmingetipaddressforuser.md) for the user specified by the *lpszUserName* parameter.</span></span>

<span data-ttu-id="2df2c-121">El programa de instalación de una DLL de administración RAS de terceros debe registrar el archivo DLL con RAS proporcionando información en la siguiente clave del registro:</span><span class="sxs-lookup"><span data-stu-id="2df2c-121">The setup program for a third-party RAS administration DLL must register the DLL with RAS by providing information under the following key in the registry:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         RAS
            AdminDll
```

<span data-ttu-id="2df2c-122">Para registrar el archivo DLL, establezca los siguientes valores bajo esta clave.</span><span class="sxs-lookup"><span data-stu-id="2df2c-122">To register the DLL, set the following values under this key.</span></span>



| <span data-ttu-id="2df2c-123">Nombre del valor</span><span class="sxs-lookup"><span data-stu-id="2df2c-123">Value name</span></span>    | <span data-ttu-id="2df2c-124">Datos del valor</span><span class="sxs-lookup"><span data-stu-id="2df2c-124">Value data</span></span>                                                                    |
|---------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="2df2c-125">*DisplayName*</span><span class="sxs-lookup"><span data-stu-id="2df2c-125">*DisplayName*</span></span> | <span data-ttu-id="2df2c-126">Una cadena **reg \_ SZ** que contiene el nombre descriptivo para mostrar del archivo dll.</span><span class="sxs-lookup"><span data-stu-id="2df2c-126">A **REG\_SZ** string that contains the user-friendly display name of the DLL.</span></span> |
| <span data-ttu-id="2df2c-127">*DLLPath*</span><span class="sxs-lookup"><span data-stu-id="2df2c-127">*DLLPath*</span></span>     | <span data-ttu-id="2df2c-128">Una cadena **reg \_ SZ** que contiene la ruta de acceso completa del archivo dll.</span><span class="sxs-lookup"><span data-stu-id="2df2c-128">A **REG\_SZ** string that contains the full path of the DLL.</span></span>                  |



 

<span data-ttu-id="2df2c-129">Por ejemplo, la entrada del registro para un archivo DLL de administración de RAS de una compañía ficticia denominada proelectrones, Inc. podría ser:</span><span class="sxs-lookup"><span data-stu-id="2df2c-129">For example, the registry entry for a RAS administration DLL from a fictional company named ProElectron, Inc. might be:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         RAS
            AdminDll
```

<span data-ttu-id="2df2c-130">*DisplayName*: **reg \_ SZ** : proelectrones ras admin dll *DLLPath*: **reg \_ SZ** : C: \\ NT \\ system32 \\ntwkadm.dll</span><span class="sxs-lookup"><span data-stu-id="2df2c-130">*DisplayName*: **REG\_SZ** : ProElectron RAS Admin DLL *DLLPath*: **REG\_SZ** : C:\\nt\\system32\\ntwkadm.dll</span></span>

<span data-ttu-id="2df2c-131">El programa de instalación de un archivo DLL de administración de RAS también debe proporcionar la funcionalidad de quitar o desinstalar.</span><span class="sxs-lookup"><span data-stu-id="2df2c-131">The setup program for a RAS administration DLL should also provide remove/uninstall functionality.</span></span> <span data-ttu-id="2df2c-132">Si un usuario quita el archivo DLL, el programa de instalación debe eliminar las entradas del registro del archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="2df2c-132">If a user removes the DLL, the setup program should delete the DLL's registry entries.</span></span>

 

 