---
title: Controlar las transferencias de archivos manualmente
description: Controlar las transferencias de archivos manualmente
ms.assetid: ff94191b-a0f2-4118-996c-d040f214fb9b
keywords:
- Windows Media Administrador de dispositivos, transferencias de archivos manuales
- Administrador de dispositivos, transferencias de archivos manuales
- Guía de programación, transferencias de archivos manuales
- aplicaciones de escritorio, transferencias de archivos manuales
- crear aplicaciones de Windows Media Administrador de dispositivos, transferencias de archivos manuales
- transferencias de archivos manuales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2bf12404e8cd83b6f0c0e4f1c8ec8b0b7bda205
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792855"
---
# <a name="handling-file-transfers-manually"></a>Controlar las transferencias de archivos manualmente

La aplicación puede implementar la interfaz [**IWMDMOperation**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation) para administrar parte del proceso de lectura o escritura. En un dispositivo de lectura, la implementación permite a la aplicación recibir bloques de datos sin procesar de un archivo de dispositivo. En una escritura en el dispositivo, permite que la aplicación envíe bloques de datos sin procesar a un archivo en el dispositivo.

En las operaciones de lectura y escritura, el método [**IWMDMOperation:: TransferObjectData**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-transferobjectdata) pasa los datos entre el equipo y el dispositivo. Para conocer la dirección de la transferencia de datos, la aplicación debe establecer una marca cuando Windows Media Administrador de dispositivos llama a [**BeginRead**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-beginread) o [**BeginWrite**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-beginwrite). Cuando se llama al método [**End**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-end) , la aplicación debe restablecer esta marca.

> [!Note]  
> Si el proveedor de servicios y el dispositivo implementan correctamente [**IMDSPObject2**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspobject2), primero llamará al método [IWMDMOperation3:: TransferObjectDataOnClearChannel](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation3-transferobjectdataonclearchannel) de la aplicación, si se implementa. Este método es una manera más eficaz de transferir datos. **TransferObjectDataOnClearChannel** se controla de la misma manera que **TransferObjectData**, salvo que los datos nunca se cifran y no tienen valores Mac para comprobar.

 

En las secciones siguientes se describe el proceso de lectura y escritura, cuando la aplicación implementa **IWMDMOperation**.

**Leer desde un dispositivo**

Al leer un archivo desde un dispositivo, Windows Media Administrador de dispositivos llama a los siguientes métodos **IWMDMOperation** en orden:

-   [**BeginRead**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-beginread) Se llama para notificar a la aplicación que se está iniciando una lectura desde el dispositivo.
-   [**TransferObjectData**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-transferobjectdata) Se llama una o varias veces. El procesamiento de datos se describe en los pasos siguientes:
    1.  **TransferObjectData** recibe un búfer, *pdata*, de tamaño *pdwSize* bytes, rellenado con datos y un equipo Mac para comprobar los datos entrantes.
    2.  La aplicación comprueba los parámetros entrantes con el equipo MAC de datos de entrada.
    3.  La aplicación descifra y Lee todos los datos de *pdata* como sea posible, y modifica el valor devuelto de *pdwSize* para indicar el número de bytes que se leyeron realmente.
    4.  La aplicación descifra los datos mediante [**CSecureChannelClient::D ecryptparam**](/previous-versions/bb231586(v=vs.85))y los almacena o los usa, según sea necesario.
    5.  **TransferObjectData** devuelve S \_ OK.
    6.  Windows Media Administrador de dispositivos sigue llamando a **TransferObjectData** hasta que la aplicación haya leído todos los datos del archivo o la aplicación devuelva el \_ usuario de WMDM e \_ \_ cancelado para cancelar la operación (en cuyo caso se cancela la lectura y Windows Media administrador de dispositivos llama a **End**).
-   [**Fin**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-end) de Se llama para notificar a la aplicación que está finalizando una lectura desde el dispositivo.

**Escribir en un dispositivo**

Al escribir un archivo en el dispositivo, Windows Media Administrador de dispositivos llama a los siguientes métodos **IWMDMOperation** en orden:

-   [**GetObjectName**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-getobjectname) Se llama para permitir que la aplicación especifique un nombre para el nuevo almacenamiento. Solo se llama a este método si la aplicación no especificó un nombre en el método de **inserción** .
-   [**GetObjectAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-getobjectattributes) Se llama para permitir que la aplicación especifique atributos para el nuevo almacenamiento en el dispositivo.
-   [**BeginWrite**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-beginwrite) Se llama para notificar que se está iniciando una escritura en el dispositivo.
-   [**GetObjectTotalSize**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-getobjecttotalsize) Se llama para recuperar el tamaño total del objeto que se está escribiendo en el dispositivo, para habilitar la optimización de la transferencia y también para proporcionar a Windows Media Administrador de dispositivos la oportunidad de cancelar la transferencia si el archivo es demasiado grande para el dispositivo.
-   [**TransferObjectData**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-transferobjectdata) Se llama una o varias veces. El procesamiento de datos se describe en los pasos siguientes:
    1.  **TransferObjectData** recibe un puntero a un búfer de tamaño *pdwSize* bytes.
    2.  La aplicación obtiene un bloque de datos que se envía al dispositivo, normalmente mediante la lectura de datos de un archivo y rellena el búfer recibido con un máximo de *pdwSize* bytes. Debe modificar *pdwSize* (si es necesario) para reflejar el número de bytes que se agregaron al búfer.
    3.  La aplicación crea un equipo MAC con todos los parámetros de método.
    4.  La aplicación cifra los datos en el búfer mediante [**CSecureChannelClient:: EncryptParam**](/previous-versions/bb231587(v=vs.85)).
    5.  **TransferObjectData** devuelve S \_ OK para indicar que hay más datos o s \_ false para indicar que no hay más datos. Si la aplicación devuelve el \_ usuario de WMDM e \_ \_ cancelado, la operación de escritura se cancela y Windows Media administrador de dispositivos llamará a **End**.
    6.  Windows Media Administrador de dispositivos sigue llamando a **TransferObjectData** siempre y cuando la aplicación devuelva el valor \_ correcto.
-   [**Fin**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-end) de Se llama para notificar que una escritura en el dispositivo está finalizando.

Para obtener un ejemplo de código, vea [cifrado y descifrado](encryption-and-decryption.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Crear una aplicación de Windows Media Administrador de dispositivos**](creating-a-windows-media-device-manager-application.md)
</dt> </dl>

 

 