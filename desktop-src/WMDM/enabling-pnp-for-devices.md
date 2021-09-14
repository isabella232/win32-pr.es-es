---
title: Habilitación de PnP para dispositivos
description: Habilitación de PnP para dispositivos
ms.assetid: 510237a9-2b74-4c2e-ad45-3f45117289a6
keywords:
- Windows Dispositivos Administrador de dispositivos,PnP
- Administrador de dispositivos, dispositivos PnP
- guía de programación, dispositivos PnP
- proveedores de servicios, dispositivos PnP
- crear proveedores de servicios, dispositivos PnP
- Dispositivos PnP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d44c7ccdfd29453c1ab28e970c1b054d1278e620
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126890348"
---
# <a name="enabling-pnp-for-devices"></a>Habilitación de PnP para dispositivos

Windows Los Administrador de dispositivos supervisan las notificaciones de llegada y eliminación de dispositivos que anuncian una interfaz de dispositivo del Reproductor de audio portátil. A la llegada de este tipo de dispositivo, Windows Media Administrador de dispositivos consulta un parámetro de dispositivo denominado *WMDMSPCLSID* para el identificador de clase del proveedor de servicios responsable de este dispositivo. Windows Media Administrador de dispositivos llama a [**IMDServiceProvider2::CreateDevice**](/windows/desktop/api/mswmdm/nf-mswmdm-imdserviceprovider2-createdevice) en este proveedor de servicios para crear un objeto de dispositivo, que se expone a la aplicación como un [**objeto IWMDMDevice.**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice)

Un proveedor de servicios puede controlar dispositivos PnP o dispositivos que no son PnP; no puede controlar ambos tipos.

Para que un dispositivo funcione con el mecanismo anterior (y, por tanto, habilite las notificaciones de llegada y eliminación para el dispositivo en aplicaciones de Windows Media Administrador de dispositivos), deben cumplirse los siguientes requisitos:

-   El controlador de dispositivo de este dispositivo debe anunciar la Windows dispositivo Administrador de dispositivos reproductor de audio portátil. El GUID de esta interfaz de dispositivo se define como:

    ```
    {0xf33fdc04, 0xd1ac, 0x4e8e, {0x9a, 0x30, 0x19, 0xbb, 0xd4, 0xb1, 0x8, 0xae} }
    ```

    

    > [!Note]  
    > Un dispositivo no debe anunciar esta interfaz si el dispositivo anuncia la interfaz Volume (definida como VolumeClassGuid o GUID \_ DEVINTERFACE \_ VOLUME en winioctl.h). Si el dispositivo anuncia la interfaz de volumen, ya está habilitado para PnP en Windows Media Administrador de dispositivos.

     

    -AND/OR-

    Se debe crear una nueva subclave del Registro para el proveedor de servicios dentro de la subclave HKEY \_ LOCAL MACHINE SOFTWARE Microsoft Windows Media Administrador de dispositivos \_ \\ \\ \\ \\ KnownDevices. Esta clave debe tener el nombre del proveedor de servicios y debe tener las dos entradas de valor REG \_ SZ siguientes:

    ```
    DeviceInterface         {25DBCE51-6C8F-4A72-8A6D-B54C2B4FC835}
    WMDMSPCLSID             {067B4B81-B1EC-489F-B111-940EBDC44EBE}
    ```

    

-   El dispositivo debe tener un parámetro de dispositivo denominado WMDMSPCLSID. El valor de este parámetro debe establecerse como el CLSID del proveedor de servicios en un formato de cadena. Para obtener más información sobre los parámetros del dispositivo, vea [Parámetros del dispositivo](device-parameters.md).

    > [!Note]  
    > El valor del parámetro debe ser el CLSID, no el ProgID del proveedor de servicios.

     

-   El proveedor de servicios para este dispositivo debe implementar la interfaz IMDServiceProvider2.
-   La clave del proveedor de servicios en HKEY \_ LOCAL MACHINE SOFTWARE Microsoft Windows Media Administrador de dispositivos Plugins SP \_ \\ \\ \\ \\ \\ \\ SPName debe contener el siguiente valor DWORD
    ```
    PnPAware    1
    ```

    

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Creación de un proveedor de servicios**](creating-a-service-provider.md)
</dt> </dl>

 

 




