---
title: Controlar las transferencias de archivos manualmente
description: Controlar las transferencias de archivos manualmente
ms.assetid: ff94191b-a0f2-4118-996c-d040f214fb9b
keywords:
- Windows Archivos Administrador de dispositivos, transferencias de archivos manuales
- Administrador de dispositivos, transferencias de archivos manuales
- guía de programación, transferencias de archivos manuales
- aplicaciones de escritorio, transferencias de archivos manuales
- creación de Windows aplicaciones Administrador de dispositivos multimedia, transferencias de archivos manuales
- transferencias de archivos manuales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b91877cf6c041ef4dfe869097863075d44034b59e980c4f1d12467342308d4f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119957425"
---
# <a name="handling-file-transfers-manually"></a>Controlar las transferencias de archivos manualmente

La aplicación puede implementar la [**interfaz IWMDMOperation para**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation) administrar parte del proceso de lectura o escritura. En una lectura desde el dispositivo, la implementación permite que la aplicación reciba bloques de datos sin procesar de un archivo de dispositivo. En un dispositivo de escritura, permite a la aplicación enviar bloques de datos sin procesar a un archivo en el dispositivo.

En las operaciones de lectura y escritura, el método [**IWMDMOperation::TransferObjectData**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-transferobjectdata) pasa los datos entre el equipo y el dispositivo. Para conocer la dirección de la transferencia de datos, la aplicación debe establecer una marca cuando Windows Media Administrador de dispositivos a [**BeginRead**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-beginread) [**o BeginWrite**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-beginwrite). Cuando se [**llama al método End,**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-end) la aplicación debe restablecer esta marca.

> [!Note]  
> Si el proveedor de servicios y el dispositivo implementan correctamente [**IMDSPObject2**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspobject2), primero llamará al método [IWMDMOperation3::TransferObjectDataOnClearChannel](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation3-transferobjectdataonclearchannel) de la aplicación, si se implementa. Este método es una manera más eficaz de transferir datos. **TransferObjectDataOnClearChannel** se controla de la misma manera que **TransferObjectData,** salvo que los datos nunca se cifran y no tienen valores MAC que comprobar.

 

En las secciones siguientes se describen tanto la lectura como el proceso de escritura, cuando la aplicación implementa **IWMDMOperation**.

**Lectura desde un dispositivo**

Al leer un archivo desde un dispositivo, Windows Media Administrador de dispositivos llama a los métodos **IWMDMOperation** siguientes en orden:

-   [**BeginRead**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-beginread) Se llama para notificar a la aplicación que se está iniciando una lectura desde el dispositivo.
-   [**TransferObjectData**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-transferobjectdata) Se le llama una o varias veces. El procesamiento de datos se describe en los pasos siguientes:
    1.  **TransferObjectData recibe** un búfer, *pData*, de tamaño *pdwSize* bytes, rellenado con datos y un EQUIPO MAC para comprobar los datos entrantes.
    2.  La aplicación comprueba los parámetros entrantes con el MAC de datos entrantes.
    3.  La aplicación descifra y lee tantos datos de *pData* como sea posible, y modifica el valor devuelto de *pdwSize* para indicar cuántos bytes se leyeron realmente.
    4.  La aplicación descifra los datos mediante [**CSecureChannelClient::D ecryptParam**](/previous-versions/bb231586(v=vs.85))y los almacena o los usa, según sea necesario.
    5.  **TransferObjectData** devuelve S \_ OK.
    6.  Windows Media Administrador de dispositivos sigue llamada a **TransferObjectData** hasta que la aplicación ha leído todos los datos del archivo o la aplicación devuelve WMDM E USER CANCELLED para cancelar la operación (en cuyo caso se cancela la lectura \_ y Windows Media Administrador de dispositivos llama a \_ \_ **End**).
-   [**Fin**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-end) Se llama para notificar a la aplicación que una lectura del dispositivo está finalizando.

**Escritura en un dispositivo**

Al escribir un archivo en el dispositivo, Windows Media Administrador de dispositivos llama a los siguientes métodos **IWMDMOperation** en orden:

-   [**GetObjectName**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-getobjectname) Se llama para permitir que la aplicación especifique un nombre para el nuevo almacenamiento. Solo se llama a este método si la aplicación no especificó un nombre en el **método Insert.**
-   [**GetObjectAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-getobjectattributes) Se llama para permitir que la aplicación especifique atributos para el nuevo almacenamiento en el dispositivo.
-   [**BeginWrite**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-beginwrite) Se llama para notificar que se está iniciando una escritura en el dispositivo.
-   [**GetObjectTotalSize**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-getobjecttotalsize) Se llama para recuperar el tamaño total del objeto que se escribe en el dispositivo, para habilitar la optimización de la transferencia y también para proporcionar a Windows Media Administrador de dispositivos una oportunidad de cancelar la transferencia si el archivo es demasiado grande para el dispositivo.
-   [**TransferObjectData**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-transferobjectdata) Se le llama una o varias veces. El procesamiento de datos se describe en los pasos siguientes:
    1.  **TransferObjectData recibe** un puntero a un búfer de bytes *pdwSize de* tamaño.
    2.  La aplicación obtiene un bloque de datos para enviar al dispositivo, normalmente leyendo datos de un archivo, y rellena el búfer recibido con hasta *pdwSize* bytes. Debe modificar *pdwSize* (si es necesario) para reflejar cuántos bytes se agregaron al búfer.
    3.  La aplicación crea un MAC de todos los parámetros de método.
    4.  La aplicación cifra los datos en el búfer mediante [**CSecureChannelClient::EncryptParam**](/previous-versions/bb231587(v=vs.85)).
    5.  **TransferObjectData** devuelve S OK para indicar que hay más datos, o S FALSE para indicar \_ que no hay más \_ datos. Si la aplicación devuelve WMDM \_ E \_ USER CANCELLED, la operación de escritura se cancela y Windows Media Administrador de dispositivos \_ llamará a **End**.
    6.  Windows Media Administrador de dispositivos sigue llamada a **TransferObjectData** siempre y cuando la aplicación devuelva S \_ OK.
-   [**Fin**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-end) Se llama para notificar que una escritura en el dispositivo está finalizando.

Para obtener un ejemplo de código, vea [Cifrado y descifrado.](encryption-and-decryption.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Creación de una Windows de Administrador de dispositivos multimedia**](creating-a-windows-media-device-manager-application.md)
</dt> </dl>

 

 