---
title: Registro del complemento DVC
description: Describe la sintaxis de la entrada del complemento de canal virtual dinámico (DVC) para el cliente Conexión a Escritorio remoto (RDC).
ms.assetid: cda4f8c9-867a-41ac-894a-4296d5912b2b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88d3660b4d9c704c9a59335cede886085f13414991dc2dc913185d407e0a3c54
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119515532"
---
# <a name="dvc-plug-in-registration"></a>Registro del complemento DVC

El complemento de canal virtual dinámico (DVC) está registrado para su uso por el cliente Conexión a Escritorio remoto (RDC) mediante uno de los métodos siguientes:

-   Invocación del método [**IMsTscAdvancedSettings::p ut \_ PluginDlls**](imstscadvancedsettings-plugindlls.md) del control Protocolo de escritorio remoto (RDP) ActiveX cliente. Varias entradas deben estar separadas por comas.
-   Escribir la entrada del complemento en la siguiente ubicación del Registro en el equipo donde se inicia el proceso de cliente Conexión a Escritorio remoto (RDC):

    **HKEY \_ CURRENT \_ USER** \\ **Software** \\ **Microsoft** \\ **Terminal Server Client** \\ **Default** \\ **AddIns** \\ **_unique plug-in name_**

    > [!Note]  
    > Debe crear la *subclave de nombre de complemento* único si no existe. El *nombre único del complemento nombre* de subclave es una cadena arbitraria que puede identificar el complemento. La cadena puede ser cualquier combinación de caracteres.

     

    En *nombre de complemento único,* debe agregar una entrada que identifique el complemento.

    Nombre de entrada = **Nombre**

    Tipo de datos = **REG \_ SZ** o **REG EXPAND \_ \_ SZ**

En ambos casos, el valor de entrada debe ajustarse a uno de los siguientes formatos:

<dl> <dt>

<span id="Plug-inDLLName__CLSID_"></span><span id="plug-indllname__clsid_"></span><span id="PLUG-INDLLNAME__CLSID_"></span>"*Plug-inDLLName*:{*CLSID*}"
</dt> <dd>

El complemento no está registrado necesariamente en el registro de Windows como un objeto de Modelo de objetos componentes (COM), pero el archivo DLL se implementa como un objeto COM en proceso. El cliente RDC cargará el archivo DLL especificado por *Plug-inDLLName* y recuperará el objeto COM directamente mediante *CLSID*.

</dd> <dt>

<span id="Plug-inDLLName"></span><span id="plug-indllname"></span><span id="PLUG-INDLLNAME"></span>"*Plug-inDLLName*"
</dt> <dd>

El archivo DLL implementa la [**función VirtualChannelGetInstance**](virtualchannelgetinstance.md) y la exporta por nombre. El cliente RDC usará la función **VirtualChannelGetInstance** para obtener punteros de interfaz [**IWTSPlugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin) para todos los complementos implementados por el archivo DLL.

</dd> <dt>

<span id="_CLSID_"></span><span id="_clsid_"></span>"{*CLSID*}"
</dt> <dd>

El cliente RDC creará una instancia del complemento como un objeto COM normal mediante [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) con *el CLSID*.

</dd> </dl>

> [!Note]  
> *Plug-inDLLName representa* la ruta de acceso completa y el nombre de archivo .dll archivo. Si el tipo de datos es **REG \_ EXPAND \_ SZ,** la ruta de acceso puede contener variables de entorno no exploradas que se expanden en tiempo de ejecución.

 

Cuando el Conexión a Escritorio remoto (RDC) finaliza su inicialización, realizará lo siguiente para cada complemento registrado:

1.  Obtenga una instancia de la [**interfaz IWTSPlugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin) para cada complemento mediante uno de los métodos descritos anteriormente.
2.  Llame al [**método Initialize**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsplugin-initialize) de cada [**interfaz IWTSPlugin.**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin)
3.  Si el cliente se conecta varias veces al mismo servidor o a otro servidor, puede haber varias llamadas a los métodos [**Conectado**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsplugin-connected) [**y**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsplugin-disconnected) Desconectado.
4.  La última llamada que el complemento debe controlar es [**Terminated**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsplugin-terminated). Es una señal de que el cliente Conexión a Escritorio remoto (RDC) está a punto de descargar el complemento.

 

 