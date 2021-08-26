---
title: Registro del administrador de protocolos
description: Debe crear al menos una entrada de valor del Registro para el administrador de protocolos para que Servicios de Escritorio remoto servicio pueda crear una instancia.
ms.assetid: 4cc7197b-88f3-4906-9b59-66587f970e2a
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f851fe74d7e22a068eccd0d901cab14d754b6b2364611bfdda2aecd68dcf224d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119988795"
---
# <a name="registering-the-protocol-manager"></a>Registro del administrador de protocolos

Debe crear al menos una entrada de valor del Registro para el administrador de protocolos para que Servicios de Escritorio remoto servicio pueda crear una instancia.

## <a name="registry-location"></a>Ubicación del registro

Cree una clave del Registro en la siguiente ubicación para cada agente de escucha [**(IWRdsProtocolListener)**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollistener)que use el protocolo. En este ejemplo, las nuevas claves de agente de escucha se *denominan MyListener1* y *MyListener2.*

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Control
            Terminal Server
               WinStations
                  RDP-Tcp
                  MyListener1
                  MyListener2
```

Como referencia, puede ver las entradas de valor en la clave de escucha **RDP-Tcp** predeterminada en esta ubicación.

## <a name="registry-value-entries"></a>Entradas de valor del Registro

La clave del agente de escucha para el protocolo debe tener una entrada de valor denominada **LoadableProtocol \_ Object**<dl> <dt>

Tipo de datos
</dt> <dd>REG_SZ</dd> </dl> of type **REG\_SZ** that contains the CLSID of the protocol manager for that listener. (The protocol manager is a COM server that implements the <a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolmanager">**Interfaz IWRdsProtocolManager).**</a> El Servicios de Escritorio remoto utiliza este CLSID para crear una instancia del administrador de protocolos para este agente de escucha después de encontrar el agente de escucha en el Registro.

Si el proveedor de protocolos usa más de un agente de escucha, el servicio Servicios de Escritorio remoto solo crea una instancia del administrador de protocolos y la usa para llamar a [**CreateListener**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolmanager-createlistener) una vez para cada agente de escucha.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Creación de un Protocolo de escritorio remoto proveedor](creating-a-custom-remote-protocol.md)
</dt> <dt>

[Secuencia de llamadas de método](method-call-sequence.md)
</dt> </dl>

 

 




