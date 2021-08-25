---
description: Esta sección contiene el material de referencia sobre la porción de las API win32 de banda ancha móvil en desuso a las API de Windows Runtime equivalentes.
title: Directrices para porte de las API win32 de banda ancha móvil a Windows Runtime API
ms.topic: reference
ms.date: 08/23/2021
ms.openlocfilehash: 4cbe0415e40f18d372fdd8b9089dbd4afe197b38
ms.sourcegitcommit: 8d7ce0c4827f8a4fd501cc6487f1a8360e944577
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/24/2021
ms.locfileid: "122767718"
---
# <a name="guidelines-for-porting-mobile-broadband-win32-apis-to-windows-runtime-apis"></a>Directrices para porte de las API win32 de banda ancha móvil a Windows Runtime API

En esta tabla se enumeran las funcionalidades Windows Runtime equivalentes para las API win32 de banda ancha móvil en desuso.

| **IMbnConnection** |  Funcionalidad equivalente Windows runtime |
| - | - |
| Conectar | ConnectivityManager.AcquireConnectionAsync |
| Desconectar | ConnectionSession.Close |
| get \_ InterfaceID | MobileBroadbandAccount.NetworkAccountId |
| GetActivationNetworkError | MobileBroadbandNetwork.ActivationNetworkError |
| GetConnectionState | WwanConnectionProfileDetails.GetNetworkRegistrationState |
| GetVoiceCallState | MobileBroadbandNetwork.GetVoiceCallSupport, PhoneCallManager.IsCallActive |
| **IMbnConnectionEvents** | |
| OnConnectComplete | NetworkStateChangeEventDetails.HasNewWwanRegistrationState: después de la notificación, el estado de registro actual se puede recuperar de WwanConnectionProfileDetails.GetNetworkRegistrationState. |
| OnConnectStateChange | NetworkStateChangeEventDetails.HasNewWwanRegistrationState: después de la notificación, el estado de registro actual se puede recuperar de WwanConnectionProfileDetails.GetNetworkRegistrationState. |
| OnDisconnectComplete | NetworkStateChangeEventDetails.HasNewWwanRegistrationState: después de la notificación, el estado de registro actual se puede recuperar de WwanConnectionProfileDetails.GetNetworkRegistrationState. |
| OnVoiceCallStateChange | PhoneCallManager.CallStateChanged |
| **IMbnConnectionProfile** | |
| Eliminar | ConnectionProfile.TryDeleteAsync |
| GetConnectionProfile | NetworkAdapter.GetConnectedProfileAsync |
| GetConnectionProfiles | NetworkInformation.GetConnectionProfiles |
| **IMbnDeviceService** | |
| CloseCommandSession | MobileBroadbandDeviceServiceCommandSession.CloseSession |
| CloseDataSession | MobileBroadbandDeviceServiceDataSession.CloseSession |
| get \_ DeviceServiceID | MobileBroadbandDeviceService.DeviceServiceId |
| OpenCommandSession | MobileBroadbandDeviceService.OpenCommandSession |
| OpenDataSession | MobileBroadbandDeviceService.OpenDataSession |
| QueryCommand | MobileBroadbandDeviceServiceCommandSession.SendQueryCommandAsync |
| QuerySupportedCommands | MobileBroadbandDeviceService.SupportedCommands |
| SetCommand | MobileBroadbandDeviceServiceCommandSession.SendSetCommandAsync |
| WriteData | MobileBroadbandDeviceServiceDataSession.WriteDataAsync |
| **IMbnDeviceServicesContext** | |
| EnumerateDeviceServices | MobileBroadbandDeviceService.SupportedCommands |
| get \_ MaxCommandSize | MobileBroadbandModem.MaxDeviceServiceCommandSizeInBytes |
| get \_ MaxDataSize | MobileBroadbandModem.MaxDeviceServiceDataSizeInByte |
| GetDeviceService | MobileBroadbandModem.GetDeviceService |
| **IMbnDeviceServicesEvents** | |
| OnReadData | MobileBroadbandDeviceServiceDataSession.DataReceived |
| **IMbnInterface** | |
| get \_ InterfaceID | MobileBroadbandAccount.NetworkAccountId |
| GetConnection | ConnectionSession obtenido de AcquireConnectionAsync |
| GetHomeProvider | MobileBroadbandModem.GetCurrentConfigurationAsync |
| GetInterfaceCapability | MobileBroadbandAccount.CurrentDeviceInformation |
| GetReadyState | MobileBroadbandDeviceInformation.NetworkDeviceStatus |
| GetSubscriberInformation | MobileBroadbandAccount.CurrentDeviceInformation |
| InEmergencyMode | MobileBroadbandModem.IsInEmergencyCallMode |
| **IMbnInterfaceEvents** | |
| OnEmergencyModeChange | MobileBroadbandModem.IsInEmergencyCallModeChanged |
| OnReadyStateChange | MobileBroadbandNetworkRegistrationStateChange |
| OnSubscriberInformationChange | MobileBroadbandAccountUpdatedEventArgs.HasDeviceInformationChanged |
| **IMbnInterfaceManager** | |
| GetInterface | MobileBroadbandModem.CurrentAccount |
| **IMbnInterfaceManagerEvents** | |
| OnInterfaceArrival | MobileBroadbandAccountWatcher.Account Agregado |
| OnInterfaceRemoval | MobileBroadbandAccountWatcher.Account |
| **IMbnMultiCarmultiCarmulti** | |
| GetCurrentCellularClass | MobileBroadbandDeviceInformation.CellularClass |
| **IMbnMultiCarevents** | |
| OnCurrentCellularClassChange | MobileBroadbandAccountUpdatedEventArgs.HasDeviceInformationChanged |
| **IMbnPin** | |
| Change | MobileBroadbandPin.ChangeAsync |
| Disable | MobileBroadbandPin.DisableAsync |
| Habilitar | MobileBroadbandPin.EnableAsync |
| Entrar | MobileBroadbandPin.EnterAsync |
| get \_ PinFormat | MobileBroadbandPin.Format |
| get \_ PinLengthMax | MobileBroadbandPin.MaxLength |
| get \_ PinLengthMin | MobileBroadbandPin.MaxLength |
| get \_ PinMode | MobileBroadbandPin.Enabled |
| get \_ PinType | MobileBroadbandPin.Type |
| GetPinManager | MobileBroadbandDeviceInformation.PinManager |
| Desbloquear | MobileBroadbandPin.UnblockAsync |
| **IMbnPinManager** | |
| GetPin | MobileBroadbandPinManager.GetPin |
| GetPinList | MobileBroadbandPinManager.SupportedPins |
| GetPinState | MobileBroadbandPin.LockState |
| **IMbnPinManagerEvents** | |
| **IMbnRadio** | |
| get \_ SoftwareRadioState | Radio.GetRadiosAsync: radio. State |
| SetSoftwareRadioState | Radio.SetStateAsync |
| **IMbnRadioEvents** | |
| OnRadioStateChange | Radio.StateChanged |
| **IMbnRegistration** | |
| GetAvailableDataClasses | MobileBroadbandDeviceInformation.DataClasses |
| GetCurrentDataClass | MobileBroadbandNetwork.RegisteredDataClass |
| GetPacketAttachNetworkError | MobileBroadbandNetwork.PacketAttachNetworkError |
| GetProviderID | MobileBroadbandNetwork.RegisteredProviderId |
| GetProviderName | MobileBroadbandNetwork.RegisteredProviderName |
| GetRegisterState | MobileBroadbandNetwork.NetworkRegistrationState |
| GetRegistrationNetworkError | MobileBroadbandNetwork.ActivationNetworkError |
| **IMbnRegistrationEvents** | |
| OnPacketServiceStateChange | MobileBroadbandNetworkRegistrationStateChange |
| OnRegisterStateChange | MobileBroadbandNetworkRegistrationStateChange |
| GetSignalStrength | ConnectionProfile.GetSignalBar / MobileBroadbandCellLte.ReferenceSignalReceivedPowerInDBm / MobileBroadbandCellGsm.ReceivedSignalStrengthInDBm |
| **IMbnSignalEvents** | |
| **IMbnSms** | |
| GetSmsConfiguration | SmsDevice2.SmscAddress, SmsDevice2.CellularClass, None para CDMAShortMessageSize y MaxMessageIndex, que no es necesario como API pública. |
| SetSmsConfiguration | SmsDevice2.SmscAddress, no se admite ninguno de los demás parámetros |
| SmsSendCdma | SendMessageAndGetResultAsync mediante CellularClass en ISmsMessageBase |
| SmsSendCdmaPdu | SendMessageAndGetResultAsync mediante Messagetype y CellularClass en ISmsMessageBase |
| SmsSendPdu | SendMessageAndGetResultAsync mediante MessageType en ISmsMessageBase |
| **IMbnSmsConfiguration** | |
| get \_ ServiceCenterAddress | SmsDevice2.SmscAddress |
| get \_ SmsFormat | SmsDevice2.CellularClass |
| put \_ ServiceCenterAddress | SmsDevice2.SmscAddress |
| **IMbnSmsEvents** | |
| OnSmsNewClass0Message | SmsMessageRegistration.MessageReceived |
| OnSmsSendComplete | SmsSendMessageResult |
| **IMbnSmsReadMsgPdu** | |
| get \_ Message | SmsTextMessage2.Body |
| get \_ PduData | SmsTextmessage2.Body |
| **IMbnSmsReadMsgTextCdma** | |
| get \_ Address | SmsTextMessage2.From |
| get \_ EncodingID | SmsTextMessage2.Encoding |
| get \_ Message | SmsTextMessage2.Body |
| get \_ Timestamp | SmsTextMessage.2Timestamp |
| **IMbnSubscriberInformation** | |
| get \_ SimIccID | MobileBroadbandDeviceInformation.SimIccId |
| get \_ SubscriberID | MobileBroadbandDeviceInformation.SubscriberId |
| obtener \_ TelephoneNumbers | MobileBroadbandDeviceInformation.TelephoneNumbers |
