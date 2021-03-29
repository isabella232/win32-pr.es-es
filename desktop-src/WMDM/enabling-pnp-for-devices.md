---
title: Habilitación de PnP para dispositivos
description: Habilitación de PnP para dispositivos
ms.assetid: 510237a9-2b74-4c2e-ad45-3f45117289a6
keywords:
- Windows Media Administrador de dispositivos, dispositivos PnP
- Administrador de dispositivos, dispositivos PnP
- Guía de programación, dispositivos PnP
- proveedores de servicios, dispositivos PnP
- creación de proveedores de servicios, dispositivos PnP
- Dispositivos PnP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d44c7ccdfd29453c1ab28e970c1b054d1278e620
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903347"
---
# <a name="enabling-pnp-for-devices"></a>Habilitación de PnP para dispositivos

Windows Media Administrador de dispositivos supervisa las notificaciones de llegada y eliminación de dispositivos que anuncian una interfaz de dispositivo del reproductor de audio portátil. Al llegar a este dispositivo, Windows Media Administrador de dispositivos consulta un parámetro de dispositivo denominado *WMDMSPCLSID* para el identificador de clase del proveedor de servicios responsable de este dispositivo. Windows Media Administrador de dispositivos llama a [**IMDServiceProvider2:: CreateDevice**](/windows/desktop/api/mswmdm/nf-mswmdm-imdserviceprovider2-createdevice) en este proveedor de servicios para crear un objeto de dispositivo, que se expone a la aplicación como un objeto [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) .

Un proveedor de servicios puede administrar dispositivos Plug and Play o dispositivos que no son Plug and Play; no puede controlar ambos tipos.

Para que un dispositivo funcione con el mecanismo anterior (y, por tanto, habilitar las notificaciones de llegada y eliminación para el dispositivo en Windows Media Administrador de dispositivos aplicaciones), deben cumplirse los siguientes requisitos:

-   El controlador de dispositivo de este dispositivo debe anunciar la interfaz de dispositivo de Windows Media Administrador de dispositivos reproductor de audio portátil. El GUID para esta interfaz de dispositivo se define de la siguiente manera:

    ```
    {0xf33fdc04, 0xd1ac, 0x4e8e, {0x9a, 0x30, 0x19, 0xbb, 0xd4, 0xb1, 0x8, 0xae} }
    ```

    

    > [!Note]  
    > Un dispositivo no debe anunciar esta interfaz si el dispositivo anuncia la interfaz de volumen (definida como volumen VolumeClassGuid o GUID \_ DEVINTERFACE \_ en winioctl. h). Si el dispositivo anuncia la interfaz de volumen, ya está habilitada para PnP en Windows Media Administrador de dispositivos.

     

    -Y/O-

    Se debe crear una nueva subclave del registro para el proveedor de servicios dentro de la subclave HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Windows Media administrador de dispositivos \\ KnownDevices. Esta clave debe tener el nombre del proveedor de servicios y debe tener las dos entradas de \_ valor reg SZ siguientes:

    ```
    DeviceInterface         {25DBCE51-6C8F-4A72-8A6D-B54C2B4FC835}
    WMDMSPCLSID             {067B4B81-B1EC-489F-B111-940EBDC44EBE}
    ```

    

-   El dispositivo debe tener un parámetro de dispositivo denominado WMDMSPCLSID. El valor de este parámetro debe establecerse como el CLSID del proveedor de servicios en un formato de cadena. Para obtener más información sobre los parámetros del dispositivo, consulte [parámetros del dispositivo](device-parameters.md).

    > [!Note]  
    > El valor del parámetro debe ser el CLSID, no el ProgID del proveedor de servicios.

     

-   El proveedor de servicios de este dispositivo debe implementar la interfaz IMDServiceProvider2.
-   La clave del proveedor de servicios en HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Windows Media administrador de dispositivos \\ plugins \\ Sp \\ SPName debe contener el siguiente valor DWORD
    ```
    PnPAware    1
    ```

    

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Creación de un proveedor de servicios**](creating-a-service-provider.md)
</dt> </dl>

 

 




