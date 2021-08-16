---
description: A continuación se enumeran los requisitos generales para la implementación del terminal conectable.
ms.assetid: 7cee19b1-ceea-494a-b576-4deede759905
title: Implementación de terminales conectables
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a75dd7b085377c8474c9a89d74a297c3ca66c6740c01c7428e7b6f250e16c5f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117762923"
---
# <a name="implementing-pluggable-terminals"></a>Implementación de terminales conectables

Los requisitos generales para la implementación del terminal conectable son:

-   El código de streaming subyacente de un terminal conectable debe coincidir con las funcionalidades de los MSP deseados.
-   El terminal debe usar DirectShow filtros para trabajar con la mayoría de los MSP (esto se supone desde aquí).
-   Los terminales de audio deben admitir PCM lineal mono de 8 kHz de 16 bits para la mayoría de los MSP.
-   El terminal debe habilitar la programación de subprocesos libre mediante la implementación [**de IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal). El terminal puede hacerlo llamando a la API COM [**CoCreateFreeThreadedMarsthread y**](/windows/win32/api/combaseapi/nf-combaseapi-cocreatefreethreadedmarshaler) agregando **IMarshal** al puntero devuelto. El destructor del objeto terminal debe llamar a [**IMarshal->Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release).
-   El terminal debe implementar o agregar cualquier interfaz específica del terminal adicional que sea adecuada.
-   La implementación del terminal debe ser segura para subprocesos.
-   La implementación del terminal \# debe incluir Termmgr.h para la definición de [**ITTerminalControl**](/windows/desktop/api/Termmgr/nn-termmgr-itterminalcontrol). Esto se suma a las bibliotecas e incluyeciones habituales que se necesitan para las aplicaciones TAPI 3 o TAPI 3 en Windows 2000 SP1.

Notas de implementación de interfaz y método:

El terminal debe implementar [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) (interfaz dual:vtable + [**IDispatch).**](/windows/win32/api/oaidl/nn-oaidl-idispatch)

[**ITTerminal::get \_ TerminalClass**](/windows/win32/api/tapi3if/nf-tapi3if-itterminal-get_terminalclass)

El terminal debe devolver una **representación BSTR** de un GUID que haya seleccionado que identifique el tipo de terminal. Asigne el **BSTR** a [**través de SysAllocString.**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) Para convertir de GUID a **BSTR,** llame [**a StringFromCLSID,**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) **SysAllocString** y [**CoTaskMemFree.**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree)

[**ITTerminal::get \_ TerminalType**](/windows/win32/api/tapi3if/nf-tapi3if-itterminal-get_terminaltype)

Por lo general, el terminal debe devolver TT \_ DYNAMIC si una aplicación implementa el terminal. Devolver TT STATIC también funcionará y devolver este valor puede ser adecuado si el terminal corresponde a un dispositivo de hardware; sin embargo, esto puede resultar confuso para los usuarios porque un terminal estático no estará presente en la enumeración de terminal estático del \_ MSP.

[**ITTerminal::get \_ State**](/windows/win32/api/tapi3if/nf-tapi3if-itterminal-get_state)

Si la implementación del terminal no limita arbitrariamente el número de secuencias a las que se puede conectar simultáneamente el terminal, el terminal siempre debe devolver TS \_ NOTINUSE.

De lo contrario, la implementación del terminal limita arbitrariamente el número de secuencias a las que se puede conectar el terminal a la vez. En este caso, el terminal debe mantener un recuento del número de flujos a los que está conectado. El terminal debe incrementar este recuento interno en una llamada [**ITTerminalControl::ConnectTerminal**](/windows/desktop/api/Termmgr/nf-termmgr-itterminalcontrol-connectterminal) correcta y disminuirlo en una llamada [**ITTerminalControl::D isconnectTerminal**](/windows/desktop/api/Termmgr/nf-termmgr-itterminalcontrol-disconnectterminal) correcta. En [**ITTerminal::get \_ State**](/windows/win32/api/tapi3if/nf-tapi3if-itterminal-get_state), debe devolver TS INUSE si este recuento es igual al número máximo de secuencias en las que se puede seleccionar el terminal a la vez; de lo contrario, debe devolver \_ TS \_ NOTINUSE. Tenga en cuenta que si el límite es uno, el recuento puede ser simplemente un valor booleano o un valor TERMINAL \_ STATE.

[**ITTerminal::get \_ Name**](/windows/win32/api/tapi3if/nf-tapi3if-itterminal-get_name)

El terminal debe devolver un **nombre BSTR** de su elección, asignado a través [**de SysAllocString.**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) Este nombre debe ser significativo para el usuario y debe localizarse.

[**ITTerminal::get \_ MediaType**](/windows/win32/api/tapi3if/nf-tapi3if-itterminal-get_mediatype)

El terminal debe devolver su tipo de medio, YA SEA TAPIMEDIATYPE \_ AUDIO o TAPIMEDIATYPE \_ VIDEO.

[**ITTerminal::get \_ Direction**](/windows/win32/api/tapi3if/nf-tapi3if-itterminal-get_direction)

El terminal devuelve el valor \_ de enumeración TERMINAL DIRECTION que indica la dirección del terminal. Si el terminal es bidireccional (por ejemplo, un puente), debe devolver TD \_ BIDIRECTIONAL.

El terminal debe implementar [**ITTerminalControl**](/windows/desktop/api/Termmgr/nn-termmgr-itterminalcontrol) (solo vtable).

[**ITTerminalControl::get \_ AddressHandle**](/windows/desktop/api/Termmgr/nf-termmgr-itterminalcontrol-get_addresshandle)

Un terminal proporcionado por la aplicación siempre debe devolver **NULL como** identificador de dirección. Esto indica al MSP que este terminal no se creó en un objeto de dirección MSP específico.

[**ITTerminalControl::ConnectTerminal**](/windows/desktop/api/Termmgr/nf-termmgr-itterminalcontrol-connectterminal)

En esta llamada, el terminal agregará sus filtros al gráfico dado y los conectará entre sí, si procede. A continuación, el terminal debe devolver los pin(s) expuestos por el terminal para la dirección de flujo especificada.

Un terminal que no admite la conexión simultánea a varias secuencias establecería una variable interna en TS INUSE al finalizar \_ correctamente este método.

El terminal puede usar el *parámetro dwTerminalDirection* de esta llamada para determinar la dirección de la secuencia a la que se está conectando. Esto es necesario para terminales bidireccionales.

> [!Note]  
> Normalmente (en las clases base de MSP y en todos los MSP conocidos), el código de secuencia msp producirá un error en la conexión si el terminal devuelve más de un pin desde una única llamada [**ConnectTerminal.**](/windows/desktop/api/Termmgr/nf-termmgr-itterminalcontrol-connectterminal) Esto está bien, porque un terminal que devuelve más de un pin durante la conexión requiere que el MSP tenga conocimientos especiales del terminal para usar los pines adicionales de forma eficaz.

 

[**ITTerminalControl::CompleteConnectTerminal**](/windows/desktop/api/Termmgr/nf-termmgr-itterminalcontrol-completeconnectterminal)

El terminal solo debe devolver S \_ OK. El terminal también puede realizar la inicialización posterior a la conexión si es necesario.

[**ITTerminalControl::D isconnectTerminal**](/windows/desktop/api/Termmgr/nf-termmgr-itterminalcontrol-disconnectterminal)

El terminal debe hacer lo que sea necesario para desconectar el terminal del resto del gráfico. Normalmente, esto implica quitar todos los filtros de los terminales del gráfico y establecer el estado del terminal en TS \_ NOTINUSE.

[**ITTerminalControl::RunRenderFilter**](/windows/desktop/api/Termmgr/nf-termmgr-itterminalcontrol-runrenderfilter)

El terminal solo debe devolver E \_ NOTIMPL.

[**ITTerminalControl::StopRenderFilter**](/windows/desktop/api/Termmgr/nf-termmgr-itterminalcontrol-stoprenderfilter)

El terminal solo debe devolver E \_ NOTIMPL.

 

 
