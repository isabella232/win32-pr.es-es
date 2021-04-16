---
title: Registro del complemento DVC
description: Describe la sintaxis de la entrada del complemento de canal virtual dinámico (DVC) del cliente Conexión a Escritorio remoto (RDC).
ms.assetid: cda4f8c9-867a-41ac-894a-4296d5912b2b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 183c73f5f9dda0321640119b2750776d207973cc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105676471"
---
# <a name="dvc-plug-in-registration"></a>Registro del complemento DVC

El complemento de canal virtual dinámico (DVC) se registra para su uso por parte del cliente de Conexión a Escritorio remoto (RDC) mediante uno de los métodos siguientes:

-   Invocar el método [**IMsTscAdvancedSettings::p UT \_ PluginDlls**](imstscadvancedsettings-plugindlls.md) del control ActiveX de protocolo de escritorio remoto (RDP). Varias entradas deben estar separadas por comas.
-   Escribir la entrada del complemento en la siguiente ubicación del registro en el equipo en el que se inicia el proceso del cliente de Conexión a Escritorio remoto (RDC):

    **HKEY \_ Software de \_ usuario actual** \\  \\ **Microsoft** \\ **Terminal Server Client** \\ **predeterminados** \\ **AddIns** \\ ***nombre de complemento único***

    > [!Note]  
    > Debe crear la subclave del *nombre del complemento único* si no existe. El nombre del *complemento único* nombre de la subclave es una cadena arbitraria que puede identificar el complemento. La cadena puede ser cualquier combinación de caracteres.

     

    En *nombre de complemento único*, debe agregar una entrada que identifique el complemento.

    Nombre de la entrada = **nombre**

    Tipo de datos = **reg \_ SZ** o **reg \_ Expand \_**

En ambos casos, el valor de entrada debe ajustarse a uno de los siguientes formatos:

<dl> <dt>

<span id="Plug-inDLLName__CLSID_"></span><span id="plug-indllname__clsid_"></span><span id="PLUG-INDLLNAME__CLSID_"></span>"*Plug-inDLLName*: {*CLSID*}"
</dt> <dd>

El complemento no se registra necesariamente en el registro de Windows como un objeto de modelo de objetos componentes (COM), pero el archivo DLL se implementa como un objeto COM en proceso. El cliente RDC cargará el archivo DLL especificado por *Plug-inDLLName* y recuperará el objeto com directamente mediante *CLSID*.

</dd> <dt>

<span id="Plug-inDLLName"></span><span id="plug-indllname"></span><span id="PLUG-INDLLNAME"></span>"*Plug-inDLLName*"
</dt> <dd>

El archivo DLL implementa la función [**VirtualChannelGetInstance**](virtualchannelgetinstance.md) y lo exporta por su nombre. El cliente RDC usará la función **VirtualChannelGetInstance** para obtener punteros de interfaz [**IWTSPlugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin) para todos los complementos implementados por el archivo dll.

</dd> <dt>

<span id="_CLSID_"></span><span id="_clsid_"></span>"{*CLSID*}"
</dt> <dd>

El cliente RDC creará una instancia del complemento como un objeto COM normal mediante [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) con el *CLSID*.

</dd> </dl>

> [!Note]  
> *Plug-inDLLName* representa la ruta de acceso completa y el nombre de archivo del archivo. dll. Si el tipo de datos es **reg \_ Expand \_ SZ**, la ruta de acceso puede contener variables de entorno no expandidas que se expandan en tiempo de ejecución.

 

Cuando el cliente de Conexión a Escritorio remoto (RDC) finaliza la inicialización, realizará lo siguiente para cada complemento registrado:

1.  Obtenga una instancia de la interfaz [**IWTSPlugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin) para cada complemento con uno de los métodos descritos anteriormente.
2.  Llame al método [**Initialize**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsplugin-initialize) de cada interfaz [**IWTSPlugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin) .
3.  Si el cliente se conecta varias veces al mismo servidor o a otro diferente, puede haber varias llamadas a los métodos [**conectados**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsplugin-connected) y [**desconectados**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsplugin-disconnected) .
4.  La última llamada que debe controlar el complemento ha [**finalizado**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsplugin-terminated). Es una señal de que el cliente Conexión a Escritorio remoto (RDC) está a punto de descargar el complemento.

 

 