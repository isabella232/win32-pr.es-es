---
title: Enumeración ExtendedDisconnectReasonCode
description: Define la información extendida sobre el motivo del control para la desconexión.
ms.assetid: E73E73B4-6C6B-4270-A1BD-947FA6D7B31B
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto enumeración ExtendedDisconnectReasonCode
topic_type:
- apiref
api_name:
- ExtendedDisconnectReasonCode
api_location:
- MsTscAx.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 657d0faee03ca37b9a5a49b95b978a24b0c8955c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676938"
---
# <a name="extendeddisconnectreasoncode-enumeration"></a><span data-ttu-id="5c0e1-104">Enumeración ExtendedDisconnectReasonCode</span><span class="sxs-lookup"><span data-stu-id="5c0e1-104">ExtendedDisconnectReasonCode enumeration</span></span>

<span data-ttu-id="5c0e1-105">Define la información extendida sobre el motivo del control para la desconexión.</span><span class="sxs-lookup"><span data-stu-id="5c0e1-105">Defines extended information about the control's reason for disconnection.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c0e1-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5c0e1-106">Syntax</span></span>


```C++
typedef enum _ExtendedDisconnectReasonCode { 
  exDiscReasonNoInfo                            = 0,
  exDiscReasonAPIInitiatedDisconnect            = 1,
  exDiscReasonAPIInitiatedLogoff                = 2,
  exDiscReasonServerIdleTimeout                 = 3,
  exDiscReasonServerLogonTimeout                = 4,
  exDiscReasonReplacedByOtherConnection         = 5,
  exDiscReasonOutOfMemory                       = 6,
  exDiscReasonServerDeniedConnection            = 7,
  exDiscReasonServerDeniedConnectionFips        = 8,
  exDiscReasonServerInsufficientPrivileges      = 9,
  exDiscReasonServerFreshCredsRequired          = 10,
  exDiscReasonRpcInitiatedDisconnectByUser      = 11,
  exDiscReasonLogoffByUser                      = 2,
  exDiscReasonLicenseInternal                   = 256,
  exDiscReasonLicenseNoLicenseServer            = 257,
  exDiscReasonLicenseNoLicense                  = 258,
  exDiscReasonLicenseErrClientMsg               = 259,
  exDiscReasonLicenseHwidDoesntMatchLicense     = 260,
  exDiscReasonLicenseErrClientLicense           = 261,
  exDiscReasonLicenseCantFinishProtocol         = 262,
  exDiscReasonLicenseClientEndedProtocol        = 263,
  exDiscReasonLicenseErrClientEncryption        = 264,
  exDiscReasonLicenseCantUpgradeLicense         = 265,
  exDiscReasonLicenseNoRemoteConnections        = 266,
  exDiscReasonLicenseCreatingLicStoreAccDenied  = 267,
  exDiscReasonRdpEncInvalidCredentials          = 768,
  exDiscReasonProtocolRangeStart                = 4096,
  exDiscReasonProtocolRangeEnd                  = 32767
} ExtendedDisconnectReasonCode;
```



## <a name="constants"></a><span data-ttu-id="5c0e1-107">Constantes</span><span class="sxs-lookup"><span data-stu-id="5c0e1-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="5c0e1-108"><span id="exDiscReasonNoInfo"></span><span id="exdiscreasonnoinfo"></span><span id="EXDISCREASONNOINFO"></span>**exDiscReasonNoInfo**</span><span class="sxs-lookup"><span data-stu-id="5c0e1-108"><span id="exDiscReasonNoInfo"></span><span id="exdiscreasonnoinfo"></span><span id="EXDISCREASONNOINFO"></span>**exDiscReasonNoInfo**</span></span>
</dt> <dd>

<span data-ttu-id="5c0e1-109">No se dispone de información adicional.</span><span class="sxs-lookup"><span data-stu-id="5c0e1-109">No additional information is available.</span></span>

</dd> <dt>

<span data-ttu-id="5c0e1-110"><span id="exDiscReasonAPIInitiatedDisconnect"></span><span id="exdiscreasonapiinitiateddisconnect"></span><span id="EXDISCREASONAPIINITIATEDDISCONNECT"></span>**exDiscReasonAPIInitiatedDisconnect**</span><span class="sxs-lookup"><span data-stu-id="5c0e1-110"><span id="exDiscReasonAPIInitiatedDisconnect"></span><span id="exdiscreasonapiinitiateddisconnect"></span><span id="EXDISCREASONAPIINITIATEDDISCONNECT"></span>**exDiscReasonAPIInitiatedDisconnect**</span></span>
</dt> <dd>

<span data-ttu-id="5c0e1-111">Una aplicación inició la desconexión.</span><span class="sxs-lookup"><span data-stu-id="5c0e1-111">An application initiated the disconnection.</span></span>

</dd> <dt>

<span data-ttu-id="5c0e1-112"><span id="exDiscReasonAPIInitiatedLogoff"></span><span id="exdiscreasonapiinitiatedlogoff"></span><span id="EXDISCREASONAPIINITIATEDLOGOFF"></span>**exDiscReasonAPIInitiatedLogoff**</span><span class="sxs-lookup"><span data-stu-id="5c0e1-112"><span id="exDiscReasonAPIInitiatedLogoff"></span><span id="exdiscreasonapiinitiatedlogoff"></span><span id="EXDISCREASONAPIINITIATEDLOGOFF"></span>**exDiscReasonAPIInitiatedLogoff**</span></span>
</dt> <dd>

<span data-ttu-id="5c0e1-113">Una aplicación cerró sesión en el cliente.</span><span class="sxs-lookup"><span data-stu-id="5c0e1-113">An application logged off the client.</span></span>

</dd> <dt>

<span data-ttu-id="5c0e1-114"><span id="exDiscReasonServerIdleTimeout"></span><span id="exdiscreasonserveridletimeout"></span><span id="EXDISCREASONSERVERIDLETIMEOUT"></span>**exDiscReasonServerIdleTimeout**</span><span class="sxs-lookup"><span data-stu-id="5c0e1-114"><span id="exDiscReasonServerIdleTimeout"></span><span id="exdiscreasonserveridletimeout"></span><span id="EXDISCREASONSERVERIDLETIMEOUT"></span>**exDiscReasonServerIdleTimeout**</span></span>
</dt> <dd>

<span data-ttu-id="5c0e1-115">El servidor ha desconectado el cliente porque el cliente ha estado inactivo durante un período de tiempo mayor que el período de tiempo de espera designado.</span><span class="sxs-lookup"><span data-stu-id="5c0e1-115">The server has disconnected the client because the client has been idle for a period of time longer than the designated time-out period.</span></span>

</dd> <dt>

<span data-ttu-id="5c0e1-116"><span id="exDiscReasonServerLogonTimeout"></span><span id="exdiscreasonserverlogontimeout"></span><span id="EXDISCREASONSERVERLOGONTIMEOUT"></span>**exDiscReasonServerLogonTimeout**</span><span class="sxs-lookup"><span data-stu-id="5c0e1-116"><span id="exDiscReasonServerLogonTimeout"></span><span id="exdiscreasonserverlogontimeout"></span><span id="EXDISCREASONSERVERLOGONTIMEOUT"></span>**exDiscReasonServerLogonTimeout**</span></span>
</dt> <dd>

<span data-ttu-id="5c0e1-117">El servidor ha desconectado el cliente porque el cliente ha superado el período designado para la conexión.</span><span class="sxs-lookup"><span data-stu-id="5c0e1-117">The server has disconnected the client because the client has exceeded the period designated for connection.</span></span>

</dd> <dt>

<span data-ttu-id="5c0e1-118"><span id="exDiscReasonReplacedByOtherConnection"></span><span id="exdiscreasonreplacedbyotherconnection"></span><span id="EXDISCREASONREPLACEDBYOTHERCONNECTION"></span>**exDiscReasonReplacedByOtherConnection**</span><span class="sxs-lookup"><span data-stu-id="5c0e1-118"><span id="exDiscReasonReplacedByOtherConnection"></span><span id="exdiscreasonreplacedbyotherconnection"></span><span id="EXDISCREASONREPLACEDBYOTHERCONNECTION"></span>**exDiscReasonReplacedByOtherConnection**</span></span>
</dt> <dd>

<span data-ttu-id="5c0e1-119">La conexión del cliente se ha reemplazado por otra conexión.</span><span class="sxs-lookup"><span data-stu-id="5c0e1-119">The client's connection was replaced by another connection.</span></span>

</dd> <dt>

<span data-ttu-id="5c0e1-120"><span id="exDiscReasonOutOfMemory"></span><span id="exdiscreasonoutofmemory"></span><span id="EXDISCREASONOUTOFMEMORY"></span>**exDiscReasonOutOfMemory**</span><span class="sxs-lookup"><span data-stu-id="5c0e1-120"><span id="exDiscReasonOutOfMemory"></span><span id="exdiscreasonoutofmemory"></span><span id="EXDISCREASONOUTOFMEMORY"></span>**exDiscReasonOutOfMemory**</span></span>
</dt> <dd>

<span data-ttu-id="5c0e1-121">No hay memoria disponible.</span><span class="sxs-lookup"><span data-stu-id="5c0e1-121">No memory is available.</span></span>

</dd> <dt>

<span data-ttu-id="5c0e1-122"><span id="exDiscReasonServerDeniedConnection"></span><span id="exdiscreasonserverdeniedconnection"></span><span id="EXDISCREASONSERVERDENIEDCONNECTION"></span>**exDiscReasonServerDeniedConnection**</span><span class="sxs-lookup"><span data-stu-id="5c0e1-122"><span id="exDiscReasonServerDeniedConnection"></span><span id="exdiscreasonserverdeniedconnection"></span><span id="EXDISCREASONSERVERDENIEDCONNECTION"></span>**exDiscReasonServerDeniedConnection**</span></span>
</dt> <dd>

<span data-ttu-id="5c0e1-123">El servidor ha denegado la conexión.</span><span class="sxs-lookup"><span data-stu-id="5c0e1-123">The server denied the connection.</span></span>

</dd> <dt>

<span data-ttu-id="5c0e1-124"><span id="exDiscReasonServerDeniedConnectionFips"></span><span id="exdiscreasonserverdeniedconnectionfips"></span><span id="EXDISCREASONSERVERDENIEDCONNECTIONFIPS"></span>**exDiscReasonServerDeniedConnectionFips**</span><span class="sxs-lookup"><span data-stu-id="5c0e1-124"><span id="exDiscReasonServerDeniedConnectionFips"></span><span id="exdiscreasonserverdeniedconnectionfips"></span><span id="EXDISCREASONSERVERDENIEDCONNECTIONFIPS"></span>**exDiscReasonServerDeniedConnectionFips**</span></span>
</dt> <dd>

<span data-ttu-id="5c0e1-125">El servidor denegó la conexión por motivos de seguridad.</span><span class="sxs-lookup"><span data-stu-id="5c0e1-125">The server denied the connection for security reasons.</span></span>

</dd> <dt>

<span data-ttu-id="5c0e1-126"><span id="exDiscReasonServerInsufficientPrivileges"></span><span id="exdiscreasonserverinsufficientprivileges"></span><span id="EXDISCREASONSERVERINSUFFICIENTPRIVILEGES"></span>**exDiscReasonServerInsufficientPrivileges**</span><span class="sxs-lookup"><span data-stu-id="5c0e1-126"><span id="exDiscReasonServerInsufficientPrivileges"></span><span id="exdiscreasonserverinsufficientprivileges"></span><span id="EXDISCREASONSERVERINSUFFICIENTPRIVILEGES"></span>**exDiscReasonServerInsufficientPrivileges**</span></span>
</dt> <dd>

<span data-ttu-id="5c0e1-127">El servidor denegó la conexión por motivos de seguridad.</span><span class="sxs-lookup"><span data-stu-id="5c0e1-127">The server denied the connection for security reasons.</span></span>

</dd> <dt>

<span data-ttu-id="5c0e1-128"><span id="exDiscReasonServerFreshCredsRequired"></span><span id="exdiscreasonserverfreshcredsrequired"></span><span id="EXDISCREASONSERVERFRESHCREDSREQUIRED"></span>**exDiscReasonServerFreshCredsRequired**</span><span class="sxs-lookup"><span data-stu-id="5c0e1-128"><span id="exDiscReasonServerFreshCredsRequired"></span><span id="exdiscreasonserverfreshcredsrequired"></span><span id="EXDISCREASONSERVERFRESHCREDSREQUIRED"></span>**exDiscReasonServerFreshCredsRequired**</span></span>
</dt> <dd>

<span data-ttu-id="5c0e1-129">Se requieren credenciales nuevas.</span><span class="sxs-lookup"><span data-stu-id="5c0e1-129">Fresh credentials are required.</span></span>

</dd> <dt>

<span data-ttu-id="5c0e1-130"><span id="exDiscReasonRpcInitiatedDisconnectByUser"></span><span id="exdiscreasonrpcinitiateddisconnectbyuser"></span><span id="EXDISCREASONRPCINITIATEDDISCONNECTBYUSER"></span>**exDiscReasonRpcInitiatedDisconnectByUser**</span><span class="sxs-lookup"><span data-stu-id="5c0e1-130"><span id="exDiscReasonRpcInitiatedDisconnectByUser"></span><span id="exdiscreasonrpcinitiateddisconnectbyuser"></span><span id="EXDISCREASONRPCINITIATEDDISCONNECTBYUSER"></span>**exDiscReasonRpcInitiatedDisconnectByUser**</span></span>
</dt> <dd>

<span data-ttu-id="5c0e1-131">La actividad de usuario ha iniciado la desconexión.</span><span class="sxs-lookup"><span data-stu-id="5c0e1-131">User activity has initiated the disconnect.</span></span>

</dd> <dt>

<span data-ttu-id="5c0e1-132"><span id="exDiscReasonLogoffByUser"></span><span id="exdiscreasonlogoffbyuser"></span><span id="EXDISCREASONLOGOFFBYUSER"></span>**exDiscReasonLogoffByUser**</span><span class="sxs-lookup"><span data-stu-id="5c0e1-132"><span id="exDiscReasonLogoffByUser"></span><span id="exdiscreasonlogoffbyuser"></span><span id="EXDISCREASONLOGOFFBYUSER"></span>**exDiscReasonLogoffByUser**</span></span>
</dt> <dd>

<span data-ttu-id="5c0e1-133">El usuario cerró sesión, desconectando la sesión.</span><span class="sxs-lookup"><span data-stu-id="5c0e1-133">The user logged off, disconnecting the session.</span></span>

</dd> <dt>

<span data-ttu-id="5c0e1-134"><span id="exDiscReasonLicenseInternal"></span><span id="exdiscreasonlicenseinternal"></span><span id="EXDISCREASONLICENSEINTERNAL"></span>**exDiscReasonLicenseInternal**</span><span class="sxs-lookup"><span data-stu-id="5c0e1-134"><span id="exDiscReasonLicenseInternal"></span><span id="exdiscreasonlicenseinternal"></span><span id="EXDISCREASONLICENSEINTERNAL"></span>**exDiscReasonLicenseInternal**</span></span>
</dt> <dd>

<span data-ttu-id="5c0e1-135">Error de licencia interno.</span><span class="sxs-lookup"><span data-stu-id="5c0e1-135">Internal licensing error.</span></span>

</dd> <dt>

<span data-ttu-id="5c0e1-136"><span id="exDiscReasonLicenseNoLicenseServer"></span><span id="exdiscreasonlicensenolicenseserver"></span><span id="EXDISCREASONLICENSENOLICENSESERVER"></span>**exDiscReasonLicenseNoLicenseServer**</span><span class="sxs-lookup"><span data-stu-id="5c0e1-136"><span id="exDiscReasonLicenseNoLicenseServer"></span><span id="exdiscreasonlicensenolicenseserver"></span><span id="EXDISCREASONLICENSENOLICENSESERVER"></span>**exDiscReasonLicenseNoLicenseServer**</span></span>
</dt> <dd>

<span data-ttu-id="5c0e1-137">No había ningún servidor de licencias disponible.</span><span class="sxs-lookup"><span data-stu-id="5c0e1-137">No license server was available.</span></span>

</dd> <dt>

<span data-ttu-id="5c0e1-138"><span id="exDiscReasonLicenseNoLicense"></span><span id="exdiscreasonlicensenolicense"></span><span id="EXDISCREASONLICENSENOLICENSE"></span>**exDiscReasonLicenseNoLicense**</span><span class="sxs-lookup"><span data-stu-id="5c0e1-138"><span id="exDiscReasonLicenseNoLicense"></span><span id="exdiscreasonlicensenolicense"></span><span id="EXDISCREASONLICENSENOLICENSE"></span>**exDiscReasonLicenseNoLicense**</span></span>
</dt> <dd>

<span data-ttu-id="5c0e1-139">No había disponible ninguna licencia de software válida.</span><span class="sxs-lookup"><span data-stu-id="5c0e1-139">No valid software license was available.</span></span>

</dd> <dt>

<span data-ttu-id="5c0e1-140"><span id="exDiscReasonLicenseErrClientMsg"></span><span id="exdiscreasonlicenseerrclientmsg"></span><span id="EXDISCREASONLICENSEERRCLIENTMSG"></span>**exDiscReasonLicenseErrClientMsg**</span><span class="sxs-lookup"><span data-stu-id="5c0e1-140"><span id="exDiscReasonLicenseErrClientMsg"></span><span id="exdiscreasonlicenseerrclientmsg"></span><span id="EXDISCREASONLICENSEERRCLIENTMSG"></span>**exDiscReasonLicenseErrClientMsg**</span></span>
</dt> <dd>

<span data-ttu-id="5c0e1-141">El equipo remoto recibió un mensaje de licencia que no era válido.</span><span class="sxs-lookup"><span data-stu-id="5c0e1-141">The remote computer received a licensing message that was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="5c0e1-142"><span id="exDiscReasonLicenseHwidDoesntMatchLicense"></span><span id="exdiscreasonlicensehwiddoesntmatchlicense"></span><span id="EXDISCREASONLICENSEHWIDDOESNTMATCHLICENSE"></span>**exDiscReasonLicenseHwidDoesntMatchLicense**</span><span class="sxs-lookup"><span data-stu-id="5c0e1-142"><span id="exDiscReasonLicenseHwidDoesntMatchLicense"></span><span id="exdiscreasonlicensehwiddoesntmatchlicense"></span><span id="EXDISCREASONLICENSEHWIDDOESNTMATCHLICENSE"></span>**exDiscReasonLicenseHwidDoesntMatchLicense**</span></span>
</dt> <dd>

<span data-ttu-id="5c0e1-143">El identificador de hardware no coincide con el designado en la licencia de software.</span><span class="sxs-lookup"><span data-stu-id="5c0e1-143">The hardware ID does not match the one designated on the software license.</span></span>

</dd> <dt>

<span data-ttu-id="5c0e1-144"><span id="exDiscReasonLicenseErrClientLicense"></span><span id="exdiscreasonlicenseerrclientlicense"></span><span id="EXDISCREASONLICENSEERRCLIENTLICENSE"></span>**exDiscReasonLicenseErrClientLicense**</span><span class="sxs-lookup"><span data-stu-id="5c0e1-144"><span id="exDiscReasonLicenseErrClientLicense"></span><span id="exdiscreasonlicenseerrclientlicense"></span><span id="EXDISCREASONLICENSEERRCLIENTLICENSE"></span>**exDiscReasonLicenseErrClientLicense**</span></span>
</dt> <dd>

<span data-ttu-id="5c0e1-145">Error de licencia de cliente.</span><span class="sxs-lookup"><span data-stu-id="5c0e1-145">Client license error.</span></span>

</dd> <dt>

<span data-ttu-id="5c0e1-146"><span id="exDiscReasonLicenseCantFinishProtocol"></span><span id="exdiscreasonlicensecantfinishprotocol"></span><span id="EXDISCREASONLICENSECANTFINISHPROTOCOL"></span>**exDiscReasonLicenseCantFinishProtocol**</span><span class="sxs-lookup"><span data-stu-id="5c0e1-146"><span id="exDiscReasonLicenseCantFinishProtocol"></span><span id="exdiscreasonlicensecantfinishprotocol"></span><span id="EXDISCREASONLICENSECANTFINISHPROTOCOL"></span>**exDiscReasonLicenseCantFinishProtocol**</span></span>
</dt> <dd>

<span data-ttu-id="5c0e1-147">Se produjeron problemas de red durante el protocolo de licencias.</span><span class="sxs-lookup"><span data-stu-id="5c0e1-147">Network problems occurred during the licensing protocol.</span></span>

</dd> <dt>

<span data-ttu-id="5c0e1-148"><span id="exDiscReasonLicenseClientEndedProtocol"></span><span id="exdiscreasonlicenseclientendedprotocol"></span><span id="EXDISCREASONLICENSECLIENTENDEDPROTOCOL"></span>**exDiscReasonLicenseClientEndedProtocol**</span><span class="sxs-lookup"><span data-stu-id="5c0e1-148"><span id="exDiscReasonLicenseClientEndedProtocol"></span><span id="exdiscreasonlicenseclientendedprotocol"></span><span id="EXDISCREASONLICENSECLIENTENDEDPROTOCOL"></span>**exDiscReasonLicenseClientEndedProtocol**</span></span>
</dt> <dd>

<span data-ttu-id="5c0e1-149">El cliente finalizó el protocolo de licencias prematuramente.</span><span class="sxs-lookup"><span data-stu-id="5c0e1-149">The client ended the licensing protocol prematurely.</span></span>

</dd> <dt>

<span data-ttu-id="5c0e1-150"><span id="exDiscReasonLicenseErrClientEncryption"></span><span id="exdiscreasonlicenseerrclientencryption"></span><span id="EXDISCREASONLICENSEERRCLIENTENCRYPTION"></span>**exDiscReasonLicenseErrClientEncryption**</span><span class="sxs-lookup"><span data-stu-id="5c0e1-150"><span id="exDiscReasonLicenseErrClientEncryption"></span><span id="exdiscreasonlicenseerrclientencryption"></span><span id="EXDISCREASONLICENSEERRCLIENTENCRYPTION"></span>**exDiscReasonLicenseErrClientEncryption**</span></span>
</dt> <dd>

<span data-ttu-id="5c0e1-151">Un mensaje de licencia se cifró incorrectamente.</span><span class="sxs-lookup"><span data-stu-id="5c0e1-151">A licensing message was encrypted incorrectly.</span></span>

</dd> <dt>

<span data-ttu-id="5c0e1-152"><span id="exDiscReasonLicenseCantUpgradeLicense"></span><span id="exdiscreasonlicensecantupgradelicense"></span><span id="EXDISCREASONLICENSECANTUPGRADELICENSE"></span>**exDiscReasonLicenseCantUpgradeLicense**</span><span class="sxs-lookup"><span data-stu-id="5c0e1-152"><span id="exDiscReasonLicenseCantUpgradeLicense"></span><span id="exdiscreasonlicensecantupgradelicense"></span><span id="EXDISCREASONLICENSECANTUPGRADELICENSE"></span>**exDiscReasonLicenseCantUpgradeLicense**</span></span>
</dt> <dd>

<span data-ttu-id="5c0e1-153">La licencia de acceso de cliente del equipo local no se pudo actualizar ni renovar.</span><span class="sxs-lookup"><span data-stu-id="5c0e1-153">The local computer's client access license could not be upgraded or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="5c0e1-154"><span id="exDiscReasonLicenseNoRemoteConnections"></span><span id="exdiscreasonlicensenoremoteconnections"></span><span id="EXDISCREASONLICENSENOREMOTECONNECTIONS"></span>**exDiscReasonLicenseNoRemoteConnections**</span><span class="sxs-lookup"><span data-stu-id="5c0e1-154"><span id="exDiscReasonLicenseNoRemoteConnections"></span><span id="exdiscreasonlicensenoremoteconnections"></span><span id="EXDISCREASONLICENSENOREMOTECONNECTIONS"></span>**exDiscReasonLicenseNoRemoteConnections**</span></span>
</dt> <dd>

<span data-ttu-id="5c0e1-155">El equipo remoto no tiene licencia para aceptar conexiones remotas.</span><span class="sxs-lookup"><span data-stu-id="5c0e1-155">The remote computer is not licensed to accept remote connections.</span></span>

</dd> <dt>

<span data-ttu-id="5c0e1-156"><span id="exDiscReasonLicenseCreatingLicStoreAccDenied"></span><span id="exdiscreasonlicensecreatinglicstoreaccdenied"></span><span id="EXDISCREASONLICENSECREATINGLICSTOREACCDENIED"></span>**exDiscReasonLicenseCreatingLicStoreAccDenied**</span><span class="sxs-lookup"><span data-stu-id="5c0e1-156"><span id="exDiscReasonLicenseCreatingLicStoreAccDenied"></span><span id="exdiscreasonlicensecreatinglicstoreaccdenied"></span><span id="EXDISCREASONLICENSECREATINGLICSTOREACCDENIED"></span>**exDiscReasonLicenseCreatingLicStoreAccDenied**</span></span>
</dt> <dd>

<span data-ttu-id="5c0e1-157">Se recibió un error de acceso denegado al crear una clave del registro para el almacén de licencias.</span><span class="sxs-lookup"><span data-stu-id="5c0e1-157">An access denied error was received while creating a registry key for the license store.</span></span>

</dd> <dt>

<span data-ttu-id="5c0e1-158"><span id="exDiscReasonRdpEncInvalidCredentials"></span><span id="exdiscreasonrdpencinvalidcredentials"></span><span id="EXDISCREASONRDPENCINVALIDCREDENTIALS"></span>**exDiscReasonRdpEncInvalidCredentials**</span><span class="sxs-lookup"><span data-stu-id="5c0e1-158"><span id="exDiscReasonRdpEncInvalidCredentials"></span><span id="exdiscreasonrdpencinvalidcredentials"></span><span id="EXDISCREASONRDPENCINVALIDCREDENTIALS"></span>**exDiscReasonRdpEncInvalidCredentials**</span></span>
</dt> <dd>

<span data-ttu-id="5c0e1-159">Se encontraron credenciales no válidas.</span><span class="sxs-lookup"><span data-stu-id="5c0e1-159">Invalid credentials were encountered.</span></span>

</dd> <dt>

<span data-ttu-id="5c0e1-160"><span id="exDiscReasonProtocolRangeStart"></span><span id="exdiscreasonprotocolrangestart"></span><span id="EXDISCREASONPROTOCOLRANGESTART"></span>**exDiscReasonProtocolRangeStart**</span><span class="sxs-lookup"><span data-stu-id="5c0e1-160"><span id="exDiscReasonProtocolRangeStart"></span><span id="exdiscreasonprotocolrangestart"></span><span id="EXDISCREASONPROTOCOLRANGESTART"></span>**exDiscReasonProtocolRangeStart**</span></span>
</dt> <dd>

<span data-ttu-id="5c0e1-161">Inicio del intervalo de errores internos del protocolo.</span><span class="sxs-lookup"><span data-stu-id="5c0e1-161">Beginning the range of internal protocol errors.</span></span> <span data-ttu-id="5c0e1-162">Compruebe el registro de eventos del servidor para obtener más detalles.</span><span class="sxs-lookup"><span data-stu-id="5c0e1-162">Check the server event log for additional details.</span></span>

</dd> <dt>

<span data-ttu-id="5c0e1-163"><span id="exDiscReasonProtocolRangeEnd"></span><span id="exdiscreasonprotocolrangeend"></span><span id="EXDISCREASONPROTOCOLRANGEEND"></span>**exDiscReasonProtocolRangeEnd**</span><span class="sxs-lookup"><span data-stu-id="5c0e1-163"><span id="exDiscReasonProtocolRangeEnd"></span><span id="exdiscreasonprotocolrangeend"></span><span id="EXDISCREASONPROTOCOLRANGEEND"></span>**exDiscReasonProtocolRangeEnd**</span></span>
</dt> <dd>

<span data-ttu-id="5c0e1-164">Finalización del intervalo de errores internos del protocolo.</span><span class="sxs-lookup"><span data-stu-id="5c0e1-164">Ending the range of internal protocol errors.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5c0e1-165">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5c0e1-165">Requirements</span></span>



| <span data-ttu-id="5c0e1-166">Requisito</span><span class="sxs-lookup"><span data-stu-id="5c0e1-166">Requirement</span></span> | <span data-ttu-id="5c0e1-167">Value</span><span class="sxs-lookup"><span data-stu-id="5c0e1-167">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5c0e1-168">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5c0e1-168">Minimum supported client</span></span><br/> | <span data-ttu-id="5c0e1-169">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5c0e1-169">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="5c0e1-170">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5c0e1-170">Minimum supported server</span></span><br/> | <span data-ttu-id="5c0e1-171">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5c0e1-171">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="5c0e1-172">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="5c0e1-172">Type library</span></span><br/>             | <dl> <span data-ttu-id="5c0e1-173"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5c0e1-173"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c0e1-174">Vea también</span><span class="sxs-lookup"><span data-stu-id="5c0e1-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c0e1-175">**ExtendedDisconnectReason**</span><span class="sxs-lookup"><span data-stu-id="5c0e1-175">**ExtendedDisconnectReason**</span></span>](imsrdpclient-extendeddisconnectreason.md)
</dt> </dl>

 

 





