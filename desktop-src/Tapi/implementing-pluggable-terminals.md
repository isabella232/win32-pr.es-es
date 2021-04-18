---
description: A continuación se enumeran los requisitos generales para la implementación del terminal acoplable.
ms.assetid: 7cee19b1-ceea-494a-b576-4deede759905
title: Implementación de terminales conectables
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 494b2f6bc5ccb214bc7101f570a4db3037fd8cae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687700"
---
# <a name="implementing-pluggable-terminals"></a>Implementación de terminales conectables

Los requisitos generales para la implementación del terminal acoplable son:

-   El código de streaming subyacente de un terminal acoplable debe coincidir con las capacidades de los MSP deseados.
-   El terminal debe usar filtros de DirectShow para trabajar con la mayoría de los MSP (esto se presupone aquí).
-   Los terminales de audio deben admitir el PCM lineal mono de 16 bits de 8 kHz para la mayoría de los MSP.
-   El terminal debe habilitar la serialización de subprocesamiento libre mediante la implementación de [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal). El terminal puede hacer esto llamando a la API de COM [**CoCreateFreeThreadedMarshaler**](/windows/win32/api/combaseapi/nf-combaseapi-cocreatefreethreadedmarshaler) y agregando **IMarshal** al puntero devuelto. El destructor del objeto terminal debe llamar a la [**versión IMarshal->**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release).
-   El terminal debe implementar o agregar interfaces adicionales específicas del terminal que sean adecuadas.
-   La implementación de terminal debe ser segura para subprocesos.
-   La implementación de terminal debe \# incluir Termmgr. h para la definición de [**ITTerminalControl**](/windows/desktop/api/Termmgr/nn-termmgr-itterminalcontrol). Además de las inclusiones y las bibliotecas habituales que son necesarias para las aplicaciones TAPI 3 o TAPI 3 en Windows 2000 SP1.

Notas sobre la implementación de la interfaz y el método:

El terminal debe implementar [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) (interfaz dual: vtable + [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)).

[**ITTerminal:: get \_ TerminalClass**](/windows/win32/api/tapi3if/nf-tapi3if-itterminal-get_terminalclass)

El terminal debe devolver una representación **BSTR** de un GUID que haya seleccionado y que identifique el tipo de terminal. Asigne el **BSTR** a través de [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring). Para convertir de GUID a **BSTR**, llame a [**StringFromCLSID**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid), **SysAllocString** y [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree).

[**ITTerminal:: get \_ TerminalType**](/windows/win32/api/tapi3if/nf-tapi3if-itterminal-get_terminaltype)

Por lo general, el terminal debe devolver TT \_ Dynamic si una aplicación implementa el terminal. La devolución \_ del TT static también funcionará y la devolución de este valor puede ser adecuada si el terminal corresponde a un dispositivo de hardware; sin embargo, esto puede resultar confuso para los usuarios porque un terminal estático no estará presente en la enumeración de terminales estática de MSP.

[**ITTerminal:: get \_ State**](/windows/win32/api/tapi3if/nf-tapi3if-itterminal-get_state)

Si la implementación de terminal no limita arbitrariamente el número de flujos a los que se puede conectar el terminal simultáneamente, el terminal siempre debe devolver NOTINUSE de TS \_ .

De lo contrario, la implementación de terminal limita arbitrariamente el número de secuencias a las que se puede conectar el terminal a la vez. En este caso, el terminal debe mantener un recuento del número de secuencias a las que está conectado. El terminal debe incrementar este recuento interno en una llamada a [**ITTerminalControl:: ConnectTerminal**](/windows/desktop/api/Termmgr/nf-termmgr-itterminalcontrol-connectterminal) correcta y disminuirlo en una llamada [**ITTerminalControl::D isconnectterminal**](/windows/desktop/api/Termmgr/nf-termmgr-itterminalcontrol-disconnectterminal) correcta. En [**ITTerminal:: get \_ State**](/windows/win32/api/tapi3if/nf-tapi3if-itterminal-get_state), debe devolver TS \_ inuse si este recuento es igual al número máximo de flujos en los que se puede seleccionar el terminal a la vez; de lo contrario, debería devolver \_ NOTINUSE de TS. Tenga en cuenta que si el límite es uno, el recuento puede ser simplemente un valor booleano o un valor de estado de TERMINAL \_ .

[**ITTerminal:: get \_ Name**](/windows/win32/api/tapi3if/nf-tapi3if-itterminal-get_name)

El terminal debe devolver un nombre **BSTR** de su elección, asignado a través de [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring). Este nombre debe ser significativo para el usuario y debe localizarse.

[**ITTerminal:: get \_ mediatype**](/windows/win32/api/tapi3if/nf-tapi3if-itterminal-get_mediatype)

El terminal debe devolver su tipo de medio, ya sea TAPIMEDIATYPE \_ audio o TAPIMEDIATYPE \_ video.

[**ITTerminal:: get \_ Direction**](/windows/win32/api/tapi3if/nf-tapi3if-itterminal-get_direction)

El terminal devuelve el \_ valor de enumeración de dirección de terminal que indica la dirección del terminal. Si el terminal es bidireccional (por ejemplo, un puente), debe devolver TD \_ bidireccionales.

El terminal debe implementar [**ITTerminalControl**](/windows/desktop/api/Termmgr/nn-termmgr-itterminalcontrol) (solo vtable).

[**ITTerminalControl:: get \_ AddressHandle**](/windows/desktop/api/Termmgr/nf-termmgr-itterminalcontrol-get_addresshandle)

Un terminal proporcionado por la aplicación siempre debe devolver **null** como identificador de dirección. Esto indica al MSP que este terminal no se ha creado en un objeto de dirección MSP específico.

[**ITTerminalControl::ConnectTerminal**](/windows/desktop/api/Termmgr/nf-termmgr-itterminalcontrol-connectterminal)

En esta llamada, el terminal agregará sus filtros al gráfico especificado y los conectará entre sí, si procede. Después, el terminal debe devolver los PIN que expone el terminal para la dirección de flujo especificada.

Un terminal que no admite conexiones simultáneas a varias secuencias establecería una variable interna para el uso \_ de TS cuando se completase correctamente este método.

El terminal puede usar el parámetro *dwTerminalDirection* de esta llamada para determinar la dirección de la secuencia a la que se está conectando. Esto es necesario para los terminales bidireccionales.

> [!Note]  
> Normalmente (en las clases base MSP y en todos los MSP conocidos), el código de secuencia MSP no podrá conectarse si el terminal devuelve más de un PIN de una única llamada [**ConnectTerminal**](/windows/desktop/api/Termmgr/nf-termmgr-itterminalcontrol-connectterminal) . Esto es correcto, ya que un terminal que devuelve más de un PIN durante la conexión requiere que el MSP tenga un conocimiento especial del terminal para que el uso de los pin adicionales sea eficaz.

 

[**ITTerminalControl::CompleteConnectTerminal**](/windows/desktop/api/Termmgr/nf-termmgr-itterminalcontrol-completeconnectterminal)

El terminal solo debe devolver S \_ correcto. El terminal también puede realizar la inicialización posterior a la conexión si es necesario.

[**ITTerminalControl::D isconnectTerminal**](/windows/desktop/api/Termmgr/nf-termmgr-itterminalcontrol-disconnectterminal)

El terminal debe hacer todo lo necesario para desconectar el terminal del resto del gráfico. Normalmente esto implica la eliminación de todos los filtros de los terminales del gráfico y el establecimiento del estado de terminal en TS \_ NOTINUSE.

[**ITTerminalControl::RunRenderFilter**](/windows/desktop/api/Termmgr/nf-termmgr-itterminalcontrol-runrenderfilter)

El terminal solo debe devolver E \_ NOTIMPL.

[**ITTerminalControl::StopRenderFilter**](/windows/desktop/api/Termmgr/nf-termmgr-itterminalcontrol-stoprenderfilter)

El terminal solo debe devolver E \_ NOTIMPL.

 

 
