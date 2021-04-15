---
description: Contiene información detallada sobre una interfaz requerida por un cliente RPC.
ms.assetid: 92e734f3-eacb-44dc-9016-88dc6e9f04b6
title: INTF_ENTRY estructura (wzcsapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- INTF_ENTRY
api_type:
- HeaderDef
api_location:
- wzcsapi.h
ms.openlocfilehash: e08efc8c95374f268efe21f963357e9c4f34ae35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543558"
---
# <a name="intf_entry-structure"></a><span data-ttu-id="64b5a-103">\_Estructura de entrada Intf</span><span class="sxs-lookup"><span data-stu-id="64b5a-103">INTF\_ENTRY structure</span></span>

<span data-ttu-id="64b5a-104">\[**Intf \_ La entrada** ya no se admite en Windows Vista y Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="64b5a-104">\[**INTF\_ENTRY** is no longer supported as of Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="64b5a-105">En su lugar, use la [API WiFi nativa](native-wifi-reference.md), que proporciona una funcionalidad similar.</span><span class="sxs-lookup"><span data-stu-id="64b5a-105">Instead, use the [Native Wifi API](native-wifi-reference.md), which provides similar functionality.</span></span> <span data-ttu-id="64b5a-106">Para obtener más información, consulte [acerca de la API WiFi nativa](about-the-native-wifi-api.md).\]</span><span class="sxs-lookup"><span data-stu-id="64b5a-106">For more information, see [About the Native Wifi API](about-the-native-wifi-api.md).\]</span></span>

<span data-ttu-id="64b5a-107">Contiene información detallada sobre una interfaz requerida por un cliente RPC.</span><span class="sxs-lookup"><span data-stu-id="64b5a-107">Contains detailed information about an interface that is required by an RPC client.</span></span>

## <a name="syntax"></a><span data-ttu-id="64b5a-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="64b5a-108">Syntax</span></span>


```C++
typedef struct {
  LPWSTR   wszGuid;
  LPWSTR   wszDescr;
  DWORD    dwContext;
  ULONG    ulMediaState;
  ULONG    ulMediaType;
  ULONG    ulPhysicalMediaType;
  INT      nInfraMode;
  INT      nAuthMode;
  INT      nWepStatus;
  DWORD    dwCtlFlags;
  DWORD    dwDynFlags;
  DWORD    dwCapabilities;
  RAW_DATA rdNicCapabilities;
  RAW_DATA rdSSID;
  RAW_DATA rdBSSID;
  RAW_DATA rdBSSIDList;
  RAW_DATA rdStSSIDList;
  RAW_DATA rdCtrlData;
} INTF_ENTRY, *PINTF_ENTRY;
```



## <a name="members"></a><span data-ttu-id="64b5a-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="64b5a-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="64b5a-110">**wszGuid**</span><span class="sxs-lookup"><span data-stu-id="64b5a-110">**wszGuid**</span></span>
</dt> <dd>

<span data-ttu-id="64b5a-111">Puntero al GUID de la interfaz que se representa como una cadena Unicode en el siguiente formato: "{xxxxxxxx-XXXX-XXXX-XXXX-XXXXXXXXXXXX}".</span><span class="sxs-lookup"><span data-stu-id="64b5a-111">A pointer to the interface GUID represented as a Unicode string in the following format: "{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}".</span></span>

</dd> <dt>

<span data-ttu-id="64b5a-112">**wszDescr**</span><span class="sxs-lookup"><span data-stu-id="64b5a-112">**wszDescr**</span></span>
</dt> <dd>

<span data-ttu-id="64b5a-113">Un puntero a una cadena que contiene la descripción de la interfaz recuperada por el servicio de configuración inalámbrica rápida (WZCSVC).</span><span class="sxs-lookup"><span data-stu-id="64b5a-113">A pointer to a string that contains the interface description that is retrieved by the Wireless Zero Configuration service (WZCSVC).</span></span>

</dd> <dt>

<span data-ttu-id="64b5a-114">**dwContext**</span><span class="sxs-lookup"><span data-stu-id="64b5a-114">**dwContext**</span></span>
</dt> <dd>

<span data-ttu-id="64b5a-115">Reservado para uso interno.</span><span class="sxs-lookup"><span data-stu-id="64b5a-115">Reserved for internal use.</span></span>

</dd> <dt>

<span data-ttu-id="64b5a-116">**ulMediaState**</span><span class="sxs-lookup"><span data-stu-id="64b5a-116">**ulMediaState**</span></span>
</dt> <dd>

<span data-ttu-id="64b5a-117">Estado actual de conexión multimedia de NDIS para la interfaz.</span><span class="sxs-lookup"><span data-stu-id="64b5a-117">The current NDIS media connect state for the interface.</span></span> <span data-ttu-id="64b5a-118">En la siguiente tabla se muestran los valores posibles.</span><span class="sxs-lookup"><span data-stu-id="64b5a-118">The following table shows the possible values.</span></span>



| <span data-ttu-id="64b5a-119">Valor</span><span class="sxs-lookup"><span data-stu-id="64b5a-119">Value</span></span>                                                                                                                                                                                                                                                  | <span data-ttu-id="64b5a-120">Significado</span><span class="sxs-lookup"><span data-stu-id="64b5a-120">Meaning</span></span>                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="MEDIA_STATE_CONNECTED_"></span><span id="media_state_connected_"></span><dl> <span data-ttu-id="64b5a-121"><dt> **\_ Estado multimedia \_ conectado**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="64b5a-121"><dt>**MEDIA\_STATE\_CONNECTED** </dt> <dt>1</dt></span></span> </dl>       | <span data-ttu-id="64b5a-122">El medio está conectado.</span><span class="sxs-lookup"><span data-stu-id="64b5a-122">The media is connected.</span></span><br/>     |
| <span id="MEDIA_STATE_DISCONNECTED"></span><span id="media_state_disconnected"></span><dl> <span data-ttu-id="64b5a-123"><dt>**Medios \_ de ESTADO \_ desconectado**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="64b5a-123"><dt>**MEDIA\_STATE\_DISCONNECTED**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="64b5a-124">El medio está desconectado.</span><span class="sxs-lookup"><span data-stu-id="64b5a-124">The media is disconnected.</span></span><br/>  |
| <span id="MEDIA_STATE_UNKNOWN"></span><span id="media_state_unknown"></span><dl> <span data-ttu-id="64b5a-125"><dt>**Medios \_ de ESTADO \_ desconocido**</dt> <dt>-1</dt></span><span class="sxs-lookup"><span data-stu-id="64b5a-125"><dt>**MEDIA\_STATE\_UNKNOWN**</dt> <dt>-1</dt></span></span> </dl>               | <span data-ttu-id="64b5a-126">No se conoce el estado del medio.</span><span class="sxs-lookup"><span data-stu-id="64b5a-126">The media state is unknown.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="64b5a-127">**ulMediaType**</span><span class="sxs-lookup"><span data-stu-id="64b5a-127">**ulMediaType**</span></span>
</dt> <dd>

<span data-ttu-id="64b5a-128">Los tipos de medios NDIS que usa actualmente la NIC.</span><span class="sxs-lookup"><span data-stu-id="64b5a-128">The NDIS media types that the NIC currently uses.</span></span> <span data-ttu-id="64b5a-129">Cuando se consulta, el valor de este miembro es **NdisMedium802 \_ 3** , tal y como se define en el archivo de encabezado *Ndispnp. h* .</span><span class="sxs-lookup"><span data-stu-id="64b5a-129">When queried, the value of this member is **NdisMedium802\_3** as defined in the *Ndispnp.h* header file.</span></span>

</dd> <dt>

<span data-ttu-id="64b5a-130">**ulPhysicalMediaType**</span><span class="sxs-lookup"><span data-stu-id="64b5a-130">**ulPhysicalMediaType**</span></span>
</dt> <dd>

<span data-ttu-id="64b5a-131">El tipo de medio NDIS para la interfaz.</span><span class="sxs-lookup"><span data-stu-id="64b5a-131">The NDIS media type for the interface.</span></span> <span data-ttu-id="64b5a-132">Cuando se consulta, el valor de este miembro es **NdisPhysicalMediumWirelessLan** , tal y como se define en el archivo de encabezado *Ndispnp. h* .</span><span class="sxs-lookup"><span data-stu-id="64b5a-132">When queried, the value of this member is **NdisPhysicalMediumWirelessLan** as defined in the *Ndispnp.h* header file.</span></span>

</dd> <dt>

<span data-ttu-id="64b5a-133">**nInfraMode**</span><span class="sxs-lookup"><span data-stu-id="64b5a-133">**nInfraMode**</span></span>
</dt> <dd>

<span data-ttu-id="64b5a-134">El modo de infraestructura 802,11 actual establecido en la interfaz.</span><span class="sxs-lookup"><span data-stu-id="64b5a-134">The current 802.11 Infrastructure Mode set on the interface.</span></span>

</dd> <dt>

<span data-ttu-id="64b5a-135">**nAuthMode**</span><span class="sxs-lookup"><span data-stu-id="64b5a-135">**nAuthMode**</span></span>
</dt> <dd>

<span data-ttu-id="64b5a-136">El modo de autenticación 802,11 actual establecido en la interfaz.</span><span class="sxs-lookup"><span data-stu-id="64b5a-136">The current 802.11 Authentication Mode set on the interface.</span></span>

<span data-ttu-id="64b5a-137">En la tabla siguiente se muestran los posibles valores para el parámetro basado en la enumeración del **\_ modo de autenticación NDIS 802 \_ 11 \_ \_** definida en el archivo de encabezado *NtDDNdis. h* .</span><span class="sxs-lookup"><span data-stu-id="64b5a-137">The following table shows the possible values for the parameter based on the **NDIS\_802\_11\_AUTHENTICATION\_MODE** enumeration defined in the *NtDDNdis.h* header file.</span></span>



| <span data-ttu-id="64b5a-138">Value</span><span class="sxs-lookup"><span data-stu-id="64b5a-138">Value</span></span>                                                                                                                                                                                                                                                                                                            | <span data-ttu-id="64b5a-139">Significado</span><span class="sxs-lookup"><span data-stu-id="64b5a-139">Meaning</span></span>                                                                                                                                                                                                                                                 |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Ndis802_11AuthModeOpen"></span><span id="ndis802_11authmodeopen"></span><span id="NDIS802_11AUTHMODEOPEN"></span><dl> <span data-ttu-id="64b5a-140"><dt>**Ndis802 \_ 11AuthModeOpen**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="64b5a-140"><dt>**Ndis802\_11AuthModeOpen**</dt> <dt>1</dt></span></span> </dl>                         | <span data-ttu-id="64b5a-141">IEEE 802,11 Open System Authentication.</span><span class="sxs-lookup"><span data-stu-id="64b5a-141">IEEE 802.11 Open System authentication.</span></span><br/>                                                                                                                                                                                                      |
| <span id="Ndis802_11AuthModeShared"></span><span id="ndis802_11authmodeshared"></span><span id="NDIS802_11AUTHMODESHARED"></span><dl> <span data-ttu-id="64b5a-142"><dt>**Ndis802 \_ 11AuthModeShared**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="64b5a-142"><dt>**Ndis802\_11AuthModeShared**</dt> <dt>2</dt></span></span> </dl>                 | <span data-ttu-id="64b5a-143">Autenticación compartida IEEE 802,11 que usa una clave de privacidad equivalente por cable (WEP) previamente compartida.</span><span class="sxs-lookup"><span data-stu-id="64b5a-143">IEEE 802.11 shared authentication that uses a pre-shared wired equivalent privacy (WEP) key.</span></span> <br/>                                                                                                                                                |
| <span id="Ndis802_11AuthModeAutoSwitch"></span><span id="ndis802_11authmodeautoswitch"></span><span id="NDIS802_11AUTHMODEAUTOSWITCH"></span><dl> <span data-ttu-id="64b5a-144"><dt>**Ndis802 \_ 11AuthModeAutoSwitch**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="64b5a-144"><dt>**Ndis802\_11AuthModeAutoSwitch**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="64b5a-145">Modo de cambio automático.</span><span class="sxs-lookup"><span data-stu-id="64b5a-145">Auto-switch mode.</span></span> <span data-ttu-id="64b5a-146">Al usar el modo de conmutador automático, la tarjeta de interfaz de red inalámbrica (NIC) intenta en primer lugar el modo de autenticación compartida.</span><span class="sxs-lookup"><span data-stu-id="64b5a-146">When using auto-switch mode, the wireless network interface card (NIC) tries shared authentication mode first.</span></span> <span data-ttu-id="64b5a-147">Si se produce un error en el modo compartido, la NIC intenta usar el modo de autenticación abierta.</span><span class="sxs-lookup"><span data-stu-id="64b5a-147">If shared mode fails, the NIC attempts to use open authentication mode.</span></span> <br/>                                    |
| <span id="Ndis802_11AuthModeWPA"></span><span id="ndis802_11authmodewpa"></span><span id="NDIS802_11AUTHMODEWPA"></span><dl> <span data-ttu-id="64b5a-148"><dt>**Ndis802 \_ 11AuthModeWPA**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="64b5a-148"><dt>**Ndis802\_11AuthModeWPA**</dt> <dt>4</dt></span></span> </dl>                             | <span data-ttu-id="64b5a-149">Seguridad de acceso protegido inalámbrico (WPA).</span><span class="sxs-lookup"><span data-stu-id="64b5a-149">Wireless Protected Access(WPA) security.</span></span> <span data-ttu-id="64b5a-150">La autenticación se realiza entre el solicitante, el autenticador y el servidor de autenticación a través de IEEE 802.1 X.</span><span class="sxs-lookup"><span data-stu-id="64b5a-150">Authentication is performed between the supplicant, authenticator, and authentication server over IEEE 802.1X.</span></span> <span data-ttu-id="64b5a-151">Las claves de cifrado son dinámicas y se derivan a través del proceso de autenticación.</span><span class="sxs-lookup"><span data-stu-id="64b5a-151">Encryption keys are dynamic and are derived through the authentication process.</span></span> <br/>     |
| <span id="Ndis802_11AuthModeWPAPSK"></span><span id="ndis802_11authmodewpapsk"></span><span id="NDIS802_11AUTHMODEWPAPSK"></span><dl> <span data-ttu-id="64b5a-152"><dt>**Ndis802 \_ 11AuthModeWPAPSK**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="64b5a-152"><dt>**Ndis802\_11AuthModeWPAPSK**</dt> <dt>5</dt></span></span> </dl>                 | <span data-ttu-id="64b5a-153">Seguridad de WPA mediante una clave previamente compartida.</span><span class="sxs-lookup"><span data-stu-id="64b5a-153">WPA security using a pre-shared key.</span></span> <span data-ttu-id="64b5a-154">La autenticación se realiza entre el solicitante y el autenticador a través de IEEE 802.1 X.</span><span class="sxs-lookup"><span data-stu-id="64b5a-154">Authentication is performed between the supplicant and authenticator over IEEE 802.1X.</span></span> <span data-ttu-id="64b5a-155">Las claves de cifrado son dinámicas y se derivan de la clave previamente compartida utilizada por el solicitante y el autenticador.</span><span class="sxs-lookup"><span data-stu-id="64b5a-155">Encryption keys are dynamic and are derived through the preshared key used by the supplicant and authenticator.</span></span> <br/> |
| <span id="Ndis802_11AuthModeWPANone"></span><span id="ndis802_11authmodewpanone"></span><span id="NDIS802_11AUTHMODEWPANONE"></span><dl> <span data-ttu-id="64b5a-156"><dt>**Ndis802 \_ 11AuthModeWPANone**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="64b5a-156"><dt>**Ndis802\_11AuthModeWPANone**</dt> <dt>6</dt></span></span> </dl>             | <span data-ttu-id="64b5a-157">Seguridad de WPA.</span><span class="sxs-lookup"><span data-stu-id="64b5a-157">WPA security.</span></span> <span data-ttu-id="64b5a-158">La autenticación se realiza mediante una clave previamente compartida sin la autenticación IEEE 802.1 X.</span><span class="sxs-lookup"><span data-stu-id="64b5a-158">Authentication is performed using a preshared key without IEEE 802.1X authentication.</span></span> <span data-ttu-id="64b5a-159">Las claves de cifrado son estáticas y se derivan de la clave previamente compartida.</span><span class="sxs-lookup"><span data-stu-id="64b5a-159">Encryption keys are static and are derived through the preshared key.</span></span> <span data-ttu-id="64b5a-160">Este modo solo es aplicable a los tipos de red ad hoc.</span><span class="sxs-lookup"><span data-stu-id="64b5a-160">This mode is applicable only to ad hoc network types.</span></span> <br/>             |
| <span id="Ndis802_11AuthModeWPA2"></span><span id="ndis802_11authmodewpa2"></span><span id="NDIS802_11AUTHMODEWPA2"></span><dl> <span data-ttu-id="64b5a-161"><dt>**Ndis802 \_ 11AuthModeWPA2**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="64b5a-161"><dt>**Ndis802\_11AuthModeWPA2**</dt> <dt>7</dt></span></span> </dl>                         | <span data-ttu-id="64b5a-162">Seguridad de WPA2.</span><span class="sxs-lookup"><span data-stu-id="64b5a-162">WPA2 security.</span></span> <span data-ttu-id="64b5a-163">La autenticación se realiza entre el solicitante, el autenticador y el servidor de autenticación a través de IEEE 802.1 X.</span><span class="sxs-lookup"><span data-stu-id="64b5a-163">Authentication is performed between the supplicant, authenticator, and authentication server over IEEE 802.1X.</span></span> <span data-ttu-id="64b5a-164">Las claves de cifrado son dinámicas y se derivan a través del proceso de autenticación.</span><span class="sxs-lookup"><span data-stu-id="64b5a-164">Encryption keys are dynamic and are derived through the authentication process.</span></span> <br/>                               |
| <span id="Ndis802_11AuthModeWPA2PSK"></span><span id="ndis802_11authmodewpa2psk"></span><span id="NDIS802_11AUTHMODEWPA2PSK"></span><dl> <span data-ttu-id="64b5a-165"><dt>**Ndis802 \_ 11AuthModeWPA2PSK**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="64b5a-165"><dt>**Ndis802\_11AuthModeWPA2PSK**</dt> <dt>8</dt></span></span> </dl>             | <span data-ttu-id="64b5a-166">Especifica la seguridad de WPA2.</span><span class="sxs-lookup"><span data-stu-id="64b5a-166">Specifies WPA2 security.</span></span> <span data-ttu-id="64b5a-167">La autenticación se realiza entre el solicitante y el autenticador a través de IEEE 802 1X.</span><span class="sxs-lookup"><span data-stu-id="64b5a-167">Authentication is performed between the supplicant and authenticator over IEEE 802 1X.</span></span> <span data-ttu-id="64b5a-168">Las claves de cifrado son dinámicas y se derivan de la clave previamente compartida utilizada por el solicitante y el autenticador.</span><span class="sxs-lookup"><span data-stu-id="64b5a-168">Encryption keys are dynamic and are derived through the preshared key used by the supplicant and authenticator.</span></span> <br/>             |
| <span id="Ndis802_11AuthModeMax"></span><span id="ndis802_11authmodemax"></span><span id="NDIS802_11AUTHMODEMAX"></span><dl> <span data-ttu-id="64b5a-169"><dt>**Ndis802 \_ 11AuthModeMax**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="64b5a-169"><dt>**Ndis802\_11AuthModeMax**</dt> <dt>9</dt></span></span> </dl>                             | <span data-ttu-id="64b5a-170">El valor máximo posible para el valor de enumeración del **\_ modo de autenticación NDIS 802 \_ 11 \_ \_** .</span><span class="sxs-lookup"><span data-stu-id="64b5a-170">The maximum possible value for the **NDIS\_802\_11\_AUTHENTICATION\_MODE** enumeration value.</span></span> <span data-ttu-id="64b5a-171">Este no es un valor válido para el modo de autenticación.</span><span class="sxs-lookup"><span data-stu-id="64b5a-171">This is not a legal value for the authentication mode.</span></span> <br/>                                                                                        |



 

</dd> <dt>

<span data-ttu-id="64b5a-172">**nWepStatus**</span><span class="sxs-lookup"><span data-stu-id="64b5a-172">**nWepStatus**</span></span>
</dt> <dd>

<span data-ttu-id="64b5a-173">El modo de cifrado de 802,11 actual establecido en la interfaz.</span><span class="sxs-lookup"><span data-stu-id="64b5a-173">The current 802.11 Encryption Mode set on the interface.</span></span>

</dd> <dt>

<span data-ttu-id="64b5a-174">**dwCtlFlags**</span><span class="sxs-lookup"><span data-stu-id="64b5a-174">**dwCtlFlags**</span></span>
</dt> <dd>

<span data-ttu-id="64b5a-175">Un valor de máscara de máscara de marcas de control que indica cómo funciona WZCSVC en la interfaz.</span><span class="sxs-lookup"><span data-stu-id="64b5a-175">A bitmask value of control flags that indicate how WZCSVC is operating on the interface.</span></span>

<span data-ttu-id="64b5a-176">En la tabla siguiente se muestran los posibles valores de bit.</span><span class="sxs-lookup"><span data-stu-id="64b5a-176">The following table shows the possible bit values.</span></span>



| <span data-ttu-id="64b5a-177">Value</span><span class="sxs-lookup"><span data-stu-id="64b5a-177">Value</span></span>                                                                                                                                                                                                                                 | <span data-ttu-id="64b5a-178">Significado</span><span class="sxs-lookup"><span data-stu-id="64b5a-178">Meaning</span></span>                                                                                                                                                                                                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="INTFCTL_CM_MASK"></span><span id="intfctl_cm_mask"></span><dl> <span data-ttu-id="64b5a-179"><dt>**INTFCTL \_ \_Máscara de cm**</dt> <dt>0x0007</dt></span><span class="sxs-lookup"><span data-stu-id="64b5a-179"><dt>**INTFCTL\_CM\_MASK**</dt> <dt>0x0007</dt></span></span> </dl>      | <span data-ttu-id="64b5a-180">Máscara de red para el modo de filtro de red.</span><span class="sxs-lookup"><span data-stu-id="64b5a-180">A bitmask for the network filter mode.</span></span> <span data-ttu-id="64b5a-181">INTFCTL \_ cm \_ Mask & dwCtlFlags generan un valor del tipo \_ infraestructura de red NDIS \_ 802 \_ 11 \_ .</span><span class="sxs-lookup"><span data-stu-id="64b5a-181">INTFCTL\_CM\_MASK & dwCtlFlags result in a value of the type NDIS\_802\_11\_NETWORK\_INFRASTRUCTURE.</span></span> <span data-ttu-id="64b5a-182">El valor resultante indica si WZCSVC solo se conecta a redes de infraestructura, redes ad hoc o a ambos tipos de redes.</span><span class="sxs-lookup"><span data-stu-id="64b5a-182">The resulting value indicates whether WZCSVC connects only to infrastructure networks, adhoc networks, or to both types of networks.</span></span><br/> |
| <span id="INTFCTL_ENABLED"></span><span id="intfctl_enabled"></span><dl> <span data-ttu-id="64b5a-183"><dt>**INTFCTL \_ HABILITAdo**</dt> <dt>0x8000</dt></span><span class="sxs-lookup"><span data-stu-id="64b5a-183"><dt>**INTFCTL\_ENABLED**</dt> <dt>0x8000</dt></span></span> </dl>       | <span data-ttu-id="64b5a-184">Indica si WZCSVC debe configurar la interfaz.</span><span class="sxs-lookup"><span data-stu-id="64b5a-184">Indicates whether WZCSVC should configure the interface.</span></span><br/>                                                                                                                                                                                                                         |
| <span id="INTFCTL_FALLBACK"></span><span id="intfctl_fallback"></span><dl> <span data-ttu-id="64b5a-185"><dt>**INTFCTL \_**</dt> <dt>0X4000</dt> de reserva</span><span class="sxs-lookup"><span data-stu-id="64b5a-185"><dt>**INTFCTL\_FALLBACK**</dt> <dt>0x4000</dt></span></span> </dl>    | <span data-ttu-id="64b5a-186">Si una red preferida no está disponible, este valor indica si WZCSVC debe configurar automáticamente la NIC para asociar a cualquier red disponible.</span><span class="sxs-lookup"><span data-stu-id="64b5a-186">If a preferred network is not available, this value indicates whether WZCSVC should automatically configure the NIC to associate to any available network.</span></span><br/>                                                                                                                       |
| <span id="INTFCTL_OIDSSUPP_"></span><span id="intfctl_oidssupp_"></span><dl> <span data-ttu-id="64b5a-187"><dt> **INTFCTL \_ OIDSSUPP**</dt> <dt>0x2000</dt></span><span class="sxs-lookup"><span data-stu-id="64b5a-187"><dt>**INTFCTL\_OIDSSUPP** </dt> <dt>0x2000</dt></span></span> </dl> | <span data-ttu-id="64b5a-188">Indica si el controlador NIC admite todos los OID 802,11 requeridos por WZCSVC para funcionar.</span><span class="sxs-lookup"><span data-stu-id="64b5a-188">Indicates whether the NIC driver supports all the 802.11 OIDs required by WZCSVC to function.</span></span><br/>                                                                                                                                                                                    |
| <span id="INTFCTL_VOLATILE_"></span><span id="intfctl_volatile_"></span><dl> <span data-ttu-id="64b5a-189"><dt> **INTFCTL \_ volatile**</dt> <dt>0x1000</dt></span><span class="sxs-lookup"><span data-stu-id="64b5a-189"><dt>**INTFCTL\_VOLATILE** </dt> <dt>0x1000</dt></span></span> </dl> | <span data-ttu-id="64b5a-190">Indica si los parámetros de servicio de esta interfaz se deben conservar en el registro.</span><span class="sxs-lookup"><span data-stu-id="64b5a-190">Indicates whether the service parameters for this interface should be retained in the registry.</span></span> <br/> <span data-ttu-id="64b5a-191">Si se establece este valor, estos parámetros son volátiles y no deben conservarse en el registro.</span><span class="sxs-lookup"><span data-stu-id="64b5a-191">If this value is set, then these parameters are volatile and should not be retained in the registry.</span></span><br/>                                                                 |
| <span id="INTFCTL_POLICY_"></span><span id="intfctl_policy_"></span><dl> <span data-ttu-id="64b5a-192"><dt>0x0800</dt> de <dt> **\_ Directiva de INTFCTL**</dt></span><span class="sxs-lookup"><span data-stu-id="64b5a-192"><dt>**INTFCTL\_POLICY** </dt> <dt>0x0800</dt></span></span> </dl>       | <span data-ttu-id="64b5a-193">Indica si una directiva de grupo inserta los parámetros de servicio para esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="64b5a-193">Indicates whether the service parameters for this interface are pushed by a group policy.</span></span><br/> <span data-ttu-id="64b5a-194">Si se establece este valor, la Directiva de grupo inserta los parámetros del servicio en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="64b5a-194">If this value is set, then the service parameters are pushed to the local computer by group policy.</span></span><br/>                                                                         |
| <span id="INTFCTL_8021XSUPP"></span><span id="intfctl_8021xsupp"></span><dl> <span data-ttu-id="64b5a-195"><dt>**INTFCTL \_ 8021XSUPP**</dt> <dt>0x1000</dt></span><span class="sxs-lookup"><span data-stu-id="64b5a-195"><dt>**INTFCTL\_8021XSUPP**</dt> <dt>0x1000</dt></span></span> </dl> | <span data-ttu-id="64b5a-196">Indica si la compatibilidad con 802.1 X está habilitada.</span><span class="sxs-lookup"><span data-stu-id="64b5a-196">Indicates whether 802.1X support is enabled.</span></span><br/>                                                                                                                                                                                                                                     |



 

</dd> <dt>

<span data-ttu-id="64b5a-197">**dwDynFlags**</span><span class="sxs-lookup"><span data-stu-id="64b5a-197">**dwDynFlags**</span></span>
</dt> <dd>

<span data-ttu-id="64b5a-198">Máscara de bits de marcas dinámicas que controlan el comportamiento dinámico (no persistente y no estático) en la interfaz.</span><span class="sxs-lookup"><span data-stu-id="64b5a-198">A bitmask of dynamic flags that control the dynamic (non-persistent and non-static) behavior on the interface.</span></span>

<span data-ttu-id="64b5a-199">Estos bits son útiles para desencadenar cambios temporales y dinámicos en la forma en que el WZCSVC actúa en la interfaz.</span><span class="sxs-lookup"><span data-stu-id="64b5a-199">These bits are useful to trigger dynamic, temporary changes in the way the WZCSVC acts on the interface.</span></span> <span data-ttu-id="64b5a-200">Ninguno de estos bits se conserva en el registro, por lo que la configuración no sobrevive al reinicio del sistema o a una secuencia de deshabilitación y habilitación de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="64b5a-200">None of these bits are persisted in the registry, so the settings won't survive a system restart or a device disable and enable sequence.</span></span>

<span data-ttu-id="64b5a-201">En la tabla siguiente se muestran los posibles valores de bit.</span><span class="sxs-lookup"><span data-stu-id="64b5a-201">The following table shows the possible bit values.</span></span>



| <span data-ttu-id="64b5a-202">Value</span><span class="sxs-lookup"><span data-stu-id="64b5a-202">Value</span></span>                                                                                                                                                                                                                            | <span data-ttu-id="64b5a-203">Significado</span><span class="sxs-lookup"><span data-stu-id="64b5a-203">Meaning</span></span>                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="INTFDYN_NOSCAN"></span><span id="intfdyn_noscan"></span><dl> <span data-ttu-id="64b5a-204"><dt>**INTFDYN \_ Noscan**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="64b5a-204"><dt>**INTFDYN\_NOSCAN**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="64b5a-205">Indica que WZCSVC no debe solicitar que la interfaz realice un examen activo, sino que use los valores almacenados en caché del controlador NIC.</span><span class="sxs-lookup"><span data-stu-id="64b5a-205">Indicates that the WZCSVC should not request the interface conduct an active scan, but instead use the cached values in the NIC driver.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="64b5a-206">**dwCapabilities**</span><span class="sxs-lookup"><span data-stu-id="64b5a-206">**dwCapabilities**</span></span>
</dt> <dd>

<span data-ttu-id="64b5a-207">Especifica las capacidades del controlador.</span><span class="sxs-lookup"><span data-stu-id="64b5a-207">Specifies the driver capabilities.</span></span>



| <span data-ttu-id="64b5a-208">Value</span><span class="sxs-lookup"><span data-stu-id="64b5a-208">Value</span></span>                                                                                                                                                                                                                                                         | <span data-ttu-id="64b5a-209">Significado</span><span class="sxs-lookup"><span data-stu-id="64b5a-209">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="INTFCAP_MAX_CIPHER_MASK"></span><span id="intfcap_max_cipher_mask"></span><dl> <span data-ttu-id="64b5a-210"><dt>**INTFCAP \_ \_ \_ Máscara de cifrado máxima**</dt> <dt>0x000000ff</dt></span><span class="sxs-lookup"><span data-stu-id="64b5a-210"><dt>**INTFCAP\_MAX\_CIPHER\_MASK**</dt> <dt>0x000000ff</dt></span></span> </dl> | <span data-ttu-id="64b5a-211">Los bits de orden inferior de este miembro se utilizan para indicar el cifrado máximo que se admite.</span><span class="sxs-lookup"><span data-stu-id="64b5a-211">The lower order bits of this member are used to indicate the maximum encryption that is supported.</span></span> <span data-ttu-id="64b5a-212">Los valores posibles son algunos de los valores de enumeración definidos en la estructura de **\_ \_ \_ \_ Estado WEP 802 11 de NDIS** en el archivo de encabezado *NtDDNdis. h* incluido en el Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="64b5a-212">The possible values are some of the enumeration values defined in the **NDIS\_802\_11\_WEP\_STATUS** structure in the *NtDDNdis.h* header file included in the Windows SDK.</span></span><br/> <span data-ttu-id="64b5a-213">El valor de 11Encryption1Enabled de Ndis802 \_ (2) indica que se admite WEP.</span><span class="sxs-lookup"><span data-stu-id="64b5a-213">The Ndis802\_11Encryption1Enabled value (2) indicates that WEP is supported.</span></span> <span data-ttu-id="64b5a-214">TKIP y AES no se admiten, y es posible que una clave de transmisión esté disponible o no.</span><span class="sxs-lookup"><span data-stu-id="64b5a-214">TKIP and AES are not supported, and a transmit key may or may not be available.</span></span> <br/> <span data-ttu-id="64b5a-215">El valor de 11Encryption2Enabled de Ndis802 \_ (9) indica que se admiten TKIP y WEP.</span><span class="sxs-lookup"><span data-stu-id="64b5a-215">The Ndis802\_11Encryption2Enabled value (9) indicates that TKIP and WEP are supported.</span></span> <span data-ttu-id="64b5a-216">No se admite AES y está disponible una clave de transmisión.</span><span class="sxs-lookup"><span data-stu-id="64b5a-216">AES is not supported, and a transmit key is available.</span></span> <br/> <span data-ttu-id="64b5a-217">El valor de 11Encryption3Enabled de Ndis802 \_ (11) indica que se admiten AES, TKIP y WEP, y que hay disponible una clave de transmisión.</span><span class="sxs-lookup"><span data-stu-id="64b5a-217">The Ndis802\_11Encryption3Enabled value (11) indicates that AES, TKIP, and WEP are supported, and a transmit key is available.</span></span> <br/> <span data-ttu-id="64b5a-218">Ndis802 \_ 11EncryptionNotSupported (8) indica que no se admite la clave WEP.</span><span class="sxs-lookup"><span data-stu-id="64b5a-218">The Ndis802\_11EncryptionNotSupported (8) indicates Indicates that the WEP key is not supported.</span></span> <br/> |
| <span id="INTFCAP_SSN"></span><span id="intfcap_ssn"></span><dl> <span data-ttu-id="64b5a-219"><dt>**INTFCAP \_ SSN**</dt> <dt>0x00000100</dt></span><span class="sxs-lookup"><span data-stu-id="64b5a-219"><dt>**INTFCAP\_SSN**</dt> <dt>0x00000100</dt></span></span> </dl>                                       | <span data-ttu-id="64b5a-220">Indica compatibilidad con la red segura simple (SSN), que es un subconjunto de 802.11 i.</span><span class="sxs-lookup"><span data-stu-id="64b5a-220">Indicates support for Simple Secure Network (SSN) which is a subset of 802.11i.</span></span> <br/> <span data-ttu-id="64b5a-221">SSN cambia la clave de cifrado periódicamente, en lugar de la estándar WEP (privacidad equivalente por cable), que usa una clave estática.</span><span class="sxs-lookup"><span data-stu-id="64b5a-221">SSN changes the encryption key periodically, as opposed to the WEP (Wired Equivalent Privacy) standard, which uses a static key.</span></span> <span data-ttu-id="64b5a-222">Para que SSN funcione, el cifrado máximo admitido debe ser al menos TKIP.</span><span class="sxs-lookup"><span data-stu-id="64b5a-222">In order for SSN to work, the maximum supported cipher should be at least TKIP.</span></span> <span data-ttu-id="64b5a-223">SSN fue desarrollado por un consorcio de proveedores en 2002 como un enfoque provisional para mejorar la seguridad de LAN inalámbrica mientras se completaba la norma IEEE 802.11 i.</span><span class="sxs-lookup"><span data-stu-id="64b5a-223">SSN was developed by a consortium of vendors in 2002 as an interim approach to improve wireless LAN security while the IEEE 802.11i standard was being completed.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="INTFCAP_80211I"></span><span id="intfcap_80211i"></span><dl> <span data-ttu-id="64b5a-224"><dt>**INTFCAP \_ 80211I**</dt> <dt>0x00000200</dt></span><span class="sxs-lookup"><span data-stu-id="64b5a-224"><dt>**INTFCAP\_80211I**</dt> <dt>0x00000200</dt></span></span> </dl>                              | <span data-ttu-id="64b5a-225">Indica compatibilidad con el estándar IEEE 802.11 i.</span><span class="sxs-lookup"><span data-stu-id="64b5a-225">Indicates support for the IEEE 802.11i standard.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |



 

</dd> <dt>

<span data-ttu-id="64b5a-226">**rdNicCapabilities**</span><span class="sxs-lookup"><span data-stu-id="64b5a-226">**rdNicCapabilities**</span></span>
</dt> <dd>

<span data-ttu-id="64b5a-227">Un conjunto de funcionalidades para 802.11 i.</span><span class="sxs-lookup"><span data-stu-id="64b5a-227">A set of capabilities for 802.11i.</span></span>

<span data-ttu-id="64b5a-228">La función [**WZCQueryInterface**](wzcqueryinterface.md) devuelve los datos de **rdNicCapabilities** cuando se llama con la marca de **\_ funcionalidades Intf** que se pasa en el parámetro *dwInflags* .</span><span class="sxs-lookup"><span data-stu-id="64b5a-228">The [**WZCQueryInterface**](wzcqueryinterface.md) function returns **rdNicCapabilities** data when called with the **INTF\_CAPABILITIES** flag passed in the *dwInflags* parameter.</span></span> <span data-ttu-id="64b5a-229">Si la llamada de función se realiza correctamente, el miembro **pdata** de la estructura de **\_ datos sin procesar** contiene una estructura de **capacidad de Intf \_ 80211 \_** .</span><span class="sxs-lookup"><span data-stu-id="64b5a-229">If the function call is successful, the **pData** member of the **RAW\_DATA** structure contains an **INTF\_80211\_CAPABILITY** structure.</span></span>

</dd> <dt>

<span data-ttu-id="64b5a-230">**rdSSID**</span><span class="sxs-lookup"><span data-stu-id="64b5a-230">**rdSSID**</span></span>
</dt> <dd>

<span data-ttu-id="64b5a-231">Datos binarios que contienen el SSID 802,11 actualmente configurado en la interfaz.</span><span class="sxs-lookup"><span data-stu-id="64b5a-231">Binary data containing the 802.11 SSID currently configured on the interface.</span></span>

<span data-ttu-id="64b5a-232">La función [**WZCQueryInterface**](wzcqueryinterface.md) devuelve los datos de **rdSSID** cuando se llama con la marca **Intf \_ SSID** pasada en el parámetro *dwInflags* .</span><span class="sxs-lookup"><span data-stu-id="64b5a-232">The [**WZCQueryInterface**](wzcqueryinterface.md) function returns **rdSSID** data when called with the **INTF\_SSID** flag passed in the *dwInflags* parameter.</span></span> <span data-ttu-id="64b5a-233">Si la llamada a la función se realiza correctamente, el miembro **dwDataLen** de la estructura de **\_ datos sin procesar** contiene el miembro **SsidLength** de una estructura de **SSID de NDIS \_ 802 \_ \_ 11** y el miembro **pdata** de la estructura de **\_ datos sin procesar** contiene el miembro **SSID** de una estructura de **\_ \_ \_ SSID 802 11 de NDIS** .</span><span class="sxs-lookup"><span data-stu-id="64b5a-233">If the function call is successful, the **dwDataLen** member of the **RAW\_DATA** structure contains the **SsidLength** member of a **NDIS\_802\_11\_SSID** structure and the **pData** member of the **RAW\_DATA** structure contains the **Ssid** member of a **NDIS\_802\_11\_SSID** structure.</span></span>

<span data-ttu-id="64b5a-234">La estructura de **\_ \_ \_ SSID NDIS 802 11** se define en el archivo de encabezado *Ntddndis. h* .</span><span class="sxs-lookup"><span data-stu-id="64b5a-234">The **NDIS\_802\_11\_SSID** structure is defined in the *Ntddndis.h* header file.</span></span>

</dd> <dt>

<span data-ttu-id="64b5a-235">**rdBSSID**</span><span class="sxs-lookup"><span data-stu-id="64b5a-235">**rdBSSID**</span></span>
</dt> <dd>

<span data-ttu-id="64b5a-236">Datos binarios que contienen el valor de BSSID 802,11 configurado en la interfaz.</span><span class="sxs-lookup"><span data-stu-id="64b5a-236">Binary data containing the 802.11 BSSID configured on the interface.</span></span>

<span data-ttu-id="64b5a-237">La función [**WZCQueryInterface**](wzcqueryinterface.md) devuelve los datos de **rdBSSID** cuando se llama con la marca **\_ BSSID Intf** pasada en el parámetro *dwInflags* .</span><span class="sxs-lookup"><span data-stu-id="64b5a-237">The [**WZCQueryInterface**](wzcqueryinterface.md) function returns **rdBSSID** data when called with the **INTF\_BSSID** flag passed in the *dwInflags* parameter.</span></span> <span data-ttu-id="64b5a-238">Si la llamada a la función se realiza correctamente, el miembro **dwDataLen** de la estructura de **\_ datos sin procesar** contiene el tamaño de una estructura de **\_ \_ \_ \_ direcciones MAC NDIS 802 11** y el miembro **pdata** de la estructura de **\_ datos sin procesar** contiene la estructura de **\_ \_ \_ \_ dirección Mac de NDIS 802 11** .</span><span class="sxs-lookup"><span data-stu-id="64b5a-238">If the function call is successful, the **dwDataLen** member of the **RAW\_DATA** structure contains the size of an **NDIS\_802\_11\_MAC\_ADDRESS** structure and the **pData** member of the **RAW\_DATA** structure contains the **NDIS\_802\_11\_MAC\_ADDRESS** structure.</span></span>

<span data-ttu-id="64b5a-239">La estructura de **\_ \_ \_ \_ direcciones MAC NDIS 802 11** se define en el archivo de encabezado *Ntddndis. h* .</span><span class="sxs-lookup"><span data-stu-id="64b5a-239">The **NDIS\_802\_11\_MAC\_ADDRESS** structure is defined in the *Ntddndis.h* header file.</span></span>

</dd> <dt>

<span data-ttu-id="64b5a-240">**rdBSSIDList**</span><span class="sxs-lookup"><span data-stu-id="64b5a-240">**rdBSSIDList**</span></span>
</dt> <dd>

<span data-ttu-id="64b5a-241">Datos binarios que contienen la lista de BSSIDs que el WZCSVC recuperó por última vez.</span><span class="sxs-lookup"><span data-stu-id="64b5a-241">Binary data that contains the list of BSSIDs that was last retrieved by WZCSVC.</span></span>

<span data-ttu-id="64b5a-242">La función [**WZCQueryInterface**](wzcqueryinterface.md) devuelve los datos de **rdBSSIDList** cuando se llama con la marca **Intf \_ BSSIDLIST** pasada en el parámetro *dwInflags* .</span><span class="sxs-lookup"><span data-stu-id="64b5a-242">The [**WZCQueryInterface**](wzcqueryinterface.md) function returns **rdBSSIDList** data when called with the **INTF\_BSSIDLIST** flag passed in the *dwInflags* parameter.</span></span> <span data-ttu-id="64b5a-243">Si la llamada de función se realiza correctamente, el miembro **dwDataLen** de la estructura de **\_ datos sin procesar** contiene la longitud del búfer con los datos devueltos y el miembro **pdata** de la estructura de **\_ datos sin procesar** contiene la estructura de la **lista de configuración de WZC \_ 802 \_ 11 \_ \_** .</span><span class="sxs-lookup"><span data-stu-id="64b5a-243">If the function call is successful, the **dwDataLen** member of the **RAW\_DATA** structure contains the length of the buffer with the returned data and the **pData** member of the **RAW\_DATA** structure contains the **WZC\_802\_11\_CONFIG\_LIST** structure.</span></span>

</dd> <dt>

<span data-ttu-id="64b5a-244">**rdStSSIDList**</span><span class="sxs-lookup"><span data-stu-id="64b5a-244">**rdStSSIDList**</span></span>
</dt> <dd>

<span data-ttu-id="64b5a-245">Datos binarios que contienen la lista de redes preferidas configuradas para esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="64b5a-245">Binary data that contains the list of preferred networks configured for this interface.</span></span>

<span data-ttu-id="64b5a-246">La función [**WZCQueryInterface**](wzcqueryinterface.md) devuelve los datos de **rdStSSIDList** cuando se llama con la marca **Intf \_ PREFLIST** pasada en el parámetro *dwInflags* .</span><span class="sxs-lookup"><span data-stu-id="64b5a-246">The [**WZCQueryInterface**](wzcqueryinterface.md) function returns **rdStSSIDList** data when called with the **INTF\_PREFLIST** flag passed in the *dwInflags* parameter.</span></span> <span data-ttu-id="64b5a-247">Si la llamada de función se realiza correctamente, el miembro **dwDataLen** de la estructura de **\_ datos sin procesar** contiene la longitud del búfer con los datos devueltos y el miembro **pdata** de la estructura de **\_ datos sin procesar** contiene la estructura de la **lista de configuración de WZC \_ 802 \_ 11 \_ \_** .</span><span class="sxs-lookup"><span data-stu-id="64b5a-247">If the function call is successful, the **dwDataLen** member of the **RAW\_DATA** structure contains the length of the buffer with the returned data and the **pData** member of the **RAW\_DATA** structure contains the **WZC\_802\_11\_CONFIG\_LIST** structure.</span></span>

<span data-ttu-id="64b5a-248">Si una de las redes preferidas está conectada actualmente, el miembro **dwCtlFlags** de la estructura de **configuración de \_ WLAN \_ de WZC** para la red tendrá establecido el bit **WZCCTL \_ media \_ Connected** (0x0400).</span><span class="sxs-lookup"><span data-stu-id="64b5a-248">If one of the preferred networks is currently connected, the **dwCtlFlags** member of the **WZC\_WLAN\_CONFIG** structure for the network will have the **WZCCTL\_MEDIA\_CONNECTED** (0x0400) bit set.</span></span>

</dd> <dt>

<span data-ttu-id="64b5a-249">**rdCtrlData**</span><span class="sxs-lookup"><span data-stu-id="64b5a-249">**rdCtrlData**</span></span>
</dt> <dd>

<span data-ttu-id="64b5a-250">Datos binarios usados con otras marcas de control, al establecer parámetros adicionales en la interfaz.</span><span class="sxs-lookup"><span data-stu-id="64b5a-250">Binary data used with other control flags, when setting additional parameters on the interface.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="64b5a-251">Observaciones</span><span class="sxs-lookup"><span data-stu-id="64b5a-251">Remarks</span></span>

<span data-ttu-id="64b5a-252">Las funciones [**WZCQueryInterface**](wzcqueryinterface.md) y [**WZCRefreshInterface**](wzcrefreshinterface.md) usan la estructura de **\_ entrada Intf** .</span><span class="sxs-lookup"><span data-stu-id="64b5a-252">The **INTF\_ENTRY** structure is used by the [**WZCQueryInterface**](wzcqueryinterface.md) and [**WZCRefreshInterface**](wzcrefreshinterface.md) functions.</span></span>

<span data-ttu-id="64b5a-253">La estructura de **\_ datos sin procesar** se define de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="64b5a-253">The **RAW\_DATA** structure is defined as follows:</span></span>


```C++
typedef struct
{
    DWORD   dwDataLen;
    LPBYTE  pData;
} RAW_DATA, *PRAW_DATA;
```



<span data-ttu-id="64b5a-254">El miembro *pdata* apunta a datos binarios.</span><span class="sxs-lookup"><span data-stu-id="64b5a-254">The *pData* member points to binary data.</span></span> <span data-ttu-id="64b5a-255">*DwDataLen* indica el número de bytes señalado por *pdata*.</span><span class="sxs-lookup"><span data-stu-id="64b5a-255">The *dwDataLen* indicates the number of bytes pointed by *pData*.</span></span>

> [!Note]  
> <span data-ttu-id="64b5a-256">El archivo de encabezado *wzcsapi. h* no está disponible en el Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="64b5a-256">The *Wzcsapi.h* header file is not available in the Windows SDK.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="64b5a-257">Requisitos</span><span class="sxs-lookup"><span data-stu-id="64b5a-257">Requirements</span></span>



| <span data-ttu-id="64b5a-258">Requisito</span><span class="sxs-lookup"><span data-stu-id="64b5a-258">Requirement</span></span> | <span data-ttu-id="64b5a-259">Value</span><span class="sxs-lookup"><span data-stu-id="64b5a-259">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="64b5a-260">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="64b5a-260">Minimum supported client</span></span><br/> | <span data-ttu-id="64b5a-261">Solo aplicaciones de escritorio de Windows XP con SP2 \[\]</span><span class="sxs-lookup"><span data-stu-id="64b5a-261">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="64b5a-262">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="64b5a-262">Minimum supported server</span></span><br/> | <span data-ttu-id="64b5a-263">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="64b5a-263">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="64b5a-264">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="64b5a-264">End of client support</span></span><br/>    | <span data-ttu-id="64b5a-265">Windows XP con SP3</span><span class="sxs-lookup"><span data-stu-id="64b5a-265">Windows XP with SP3</span></span><br/>                                                       |
| <span data-ttu-id="64b5a-266">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="64b5a-266">End of server support</span></span><br/>    | <span data-ttu-id="64b5a-267">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="64b5a-267">Windows Server 2003</span></span><br/>                                                       |
| <span data-ttu-id="64b5a-268">Encabezado</span><span class="sxs-lookup"><span data-stu-id="64b5a-268">Header</span></span><br/>                   | <dl> <span data-ttu-id="64b5a-269"><dt>Wzcsapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="64b5a-269"><dt>Wzcsapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="64b5a-270">Vea también</span><span class="sxs-lookup"><span data-stu-id="64b5a-270">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64b5a-271">**WZCEnumInterfaces**</span><span class="sxs-lookup"><span data-stu-id="64b5a-271">**WZCEnumInterfaces**</span></span>](wzcenuminterfaces.md)
</dt> <dt>

[<span data-ttu-id="64b5a-272">**WZCQueryInterface**</span><span class="sxs-lookup"><span data-stu-id="64b5a-272">**WZCQueryInterface**</span></span>](wzcqueryinterface.md)
</dt> <dt>

[<span data-ttu-id="64b5a-273">**WZCRefreshInterface**</span><span class="sxs-lookup"><span data-stu-id="64b5a-273">**WZCRefreshInterface**</span></span>](wzcrefreshinterface.md)
</dt> </dl>

 

 




