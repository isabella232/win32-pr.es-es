---
description: En esta sección se explica cómo recuperar el marcado MathML del control de entrada matemática mediante el Active Template Library (ATL) y el modelo de objetos componentes (COM).
ms.assetid: 352d2a0c-8275-4fe4-b523-4c74126ffadf
title: Recepción de la entrada del Control de entrada matemática
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50325b8e9980907b91f4cd6400ed6cfd0ef3f04367a2bc753e5d4065e189bc44
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118449335"
---
# <a name="receiving-input-from-the-math-input-control"></a>Recepción de la entrada del Control de entrada matemática

En esta sección se explica cómo recuperar el marcado MathML del control de entrada matemática mediante el Active Template Library (ATL) y el modelo de objetos componentes (COM).

Para recuperar la ecuación matemática reconocida del control de entrada matemática, puede invalidar el comportamiento que se produce cuando se presiona el botón insertar. Para ello, deberá configurar un controlador de eventos que implemente los distintos eventos admitidos por la [**\_ interfaz IMathInputControlEvents.**](/windows/win32/api/micaut/nn-micaut-_imathinputcontrolevents) La configuración del controlador de eventos implica realizar los pasos siguientes para los eventos que desea admitir (inserte en este caso).

-   [Creación de una clase de plantilla que contiene receptores de eventos](#create-a-template-class-that-contains-event-sinks)
-   [Configuración de los controladores de eventos](#set-up-the-event-handlers)
-   [Heredar la clase de controlador de eventos de la clase principal](#inherit-the-event-handler-class-in-your-main-class)
-   [Inicialice la clase para heredar los receptores de eventos.](#initialize-your-class-to-inherit-the-event-sinks)

## <a name="create-a-template-class-that-contains-event-sinks"></a>Creación de una clase de plantilla que contiene receptores de eventos

Al implementar un receptor de eventos que usa el control de entrada matemático, primero debe especificar un identificador de receptor. A continuación, debe crear una clase de plantilla que herede de las interfaces de eventos event, event control handler e math input control. El código siguiente muestra cómo establecer un identificador de receptor y crear una clase de plantilla, CMathInputControlEventHandler, que hereda de las interfaces necesarias. Esta clase de plantilla también está configurada para tener un puntero de interfaz desconocido privado que se usará para pasarle el control de entrada matemático en la inicialización y el miembro m ulAdviseCount para contar el número de llamadas que se aconsejan o \_ desvía.


```
  
#pragma once
static const int MATHINPUTCONTROL_SINK_ID = 1 ;

template <class T>
class ATL_NO_VTABLE CMathInputControlEventHandler :
    public IDispEventSimpleImpl<MATHINPUTCONTROL_SINK_ID, CMathInputControlEventHandler<T>, &__uuidof(_IMathInputControlEvents)>
{
private:
    IUnknown    *m_pUnknown;
    ULONG m_ulAdviseCount;
    CDialog *m_pMain;

```



> [!Note]  
> El miembro **m \_ pMain** debe ser diferente en la implementación si no usa un cuadro de diálogo.

 

Ahora que tiene la clase de plantilla básica, debe proporcionar una declaración de reenvío para los controladores de eventos que va a invalidar y, a continuación, debe configurar un mapa de receptor para los eventos que va a controlar. El código siguiente muestra cómo configurar controladores de eventos para el método [**Insert,**](/previous-versions/windows/desktop/legacy/dd317352(v=vs.85)) al que se llama cuando un usuario hace clic en el botón insertar en el control de entrada matemática, y el método [**Close,**](/previous-versions/windows/desktop/legacy/dd317351(v=vs.85)) al que se llama cuando un usuario hace clic en el botón cancelar del control de entrada matemática.


```
  
public:
    static const _ATL_FUNC_INFO OnMICInsertInfo; // = {CC_STDCALL, VT_I4, 1, {VT_BSTR}};
    static const _ATL_FUNC_INFO OnMICCloseInfo;  // = {CC_STDCALL, VT_I4, 0, {VT_EMPTY}};

    BEGIN_SINK_MAP(CMathInputControlEventHandler)
        SINK_ENTRY_INFO(MATHINPUTCONTROL_SINK_ID, __uuidof(_IMathInputControlEvents), DISPID_MICInsert, OnMICInsert, const_cast<_ATL_FUNC_INFO*>(&OnMICInsertInfo))
        SINK_ENTRY_INFO(MATHINPUTCONTROL_SINK_ID, __uuidof(_IMathInputControlEvents), DISPID_MICClose, OnMICClose, const_cast<_ATL_FUNC_INFO*>(&OnMICCloseInfo))  
    END_SINK_MAP()
```



Puesto que trabajará con el control de entrada matemática, será útil establecer una referencia interna a la interfaz correspondiente. La siguiente función de utilidad se crea en la clase de ejemplo para establecer esta referencia.


```
    
  HRESULT Initialize(IUnknown *pUnknown, CDialog *pMain)
  {
    m_pMain  = pMain;
    m_pUnknown = pUnknown;
    m_ulAdviseCount = 0;
    return S_OK;
  }
  
```



## <a name="set-up-the-event-handlers"></a>Configuración de los controladores de eventos

Una vez configurados los receptores de eventos, deberá crear las implementaciones de los receptores de eventos. En ambos métodos del ejemplo de código siguiente, los receptores de eventos recuperan un identificador para la interfaz de control de entrada matemática. En la [**función Insert,**](/previous-versions/windows/desktop/legacy/dd317352(v=vs.85)) el resultado del reconocimiento se muestra como MathML y el control está oculto. En la [**función Close,**](/previous-versions/windows/desktop/legacy/dd317351(v=vs.85)) el control de entrada matemático está oculto.


```
  
    // Methods
    HRESULT __stdcall OnMICInsert( BSTR bstrRecoResult)
    {
        CComQIPtr<IMathInputControl> spMIC(m_pUnknown);
        HRESULT hr=S_OK;
        if (spMIC)
        {           
            MessageBox(NULL,bstrRecoResult,L"Recognition Result",MB_OK);
            hr = spMIC->Hide();
            return hr;  
        }
        return E_FAIL;          
    }

    HRESULT __stdcall OnMICClose()
    {
        CComPtr<IMathInputControl> spMIC;
        HRESULT hr = m_pUnknown->QueryInterface<IMathInputControl>(&spMIC);
        if (SUCCEEDED(hr))
        {           
            hr = spMIC->Hide();
            return hr;  
        }
        return hr;                  
    }
};  
```



## <a name="inherit-the-event-handler-class-in-your-main-class"></a>Heredar la clase de controlador de eventos de la clase principal

Una vez implementada la clase de plantilla, deberá heredarla en la clase en la que va a configurar el control de entrada matemática. Para los fines de esta guía, esta clase es un diálogo, CMIC \_ TEST \_ EVENTSDlg. En el encabezado del cuadro de diálogo, se deben incluir los encabezados necesarios y se debe heredar la clase de plantilla que creó. La clase en la que hereda y los controladores de eventos deben tener declaraciones de reenvío para que se pueda implementar la plantilla. En el ejemplo de código siguiente se muestra cómo se hace esto.


```
#pragma once
#include <atlbase.h>
#include <atlwin.h>

// include for MIC
#include "micaut.h"

// include for event sinks
#include <iacom.h>
#include "mathinputcontroleventhandler.h"

class CMIC_TEST_EVENTSDlg;

const _ATL_FUNC_INFO CMathInputControlEventHandler<CMIC_TEST_EVENTSDlg>::OnMICInsertInfo = {CC_STDCALL, VT_I4, 1, {VT_BSTR}};
const _ATL_FUNC_INFO CMathInputControlEventHandler<CMIC_TEST_EVENTSDlg>::OnMICCloseInfo = {CC_STDCALL, VT_I4, 0, {VT_EMPTY}};

// CMIC_TEST_EVENTSDlg dialog
class CMIC_TEST_EVENTSDlg : public CDialog,
    public CMathInputControlEventHandler<CMIC_TEST_EVENTSDlg>
{
  public:
  CComPtr<IMathInputControl> m_spMIC; // Math Input Control

  
```



> [!Note]  
> El tipo de plantilla, **CMIC \_ TEST \_ EventsDlg**, será diferente a menos que haya llamado a la clase igual que en el ejemplo.

 

## <a name="initialize-your-class-to-inherit-the-event-sinks"></a>Inicialice la clase para heredar los receptores de eventos.

Una vez que haya configurado la clase para heredar de la clase de plantilla, estará listo para configurarla para controlar eventos. Esto conste de inicializar la clase para que tenga un identificador para el control de entrada matemático y la clase que realiza la llamada. Además, el control de entrada matemático desde el que controlar eventos se debe enviar al método DispEventAdvise que hereda la clase de ejemplo CMathInputControlEventHandler. Se llama al código siguiente desde el método OnInitDialog de la clase de ejemplo para realizar estas acciones.


```
// includes for implementation
#include "micaut_i.c"

// include for event handler
#include "mathinputcontroleventhandler.h"

...

OnInitDialog{
  ...

  // TODO: Add extra initialization here
  CoInitialize(NULL);
  HRESULT hr = g_spMIC.CoCreateInstance(CLSID_MathInputControl);
  if (SUCCEEDED(hr)){
    hr = CMathInputControlEventHandler<CMIC_TEST_EVENTSDlg>::Initialize(m_spMIC, this);
      if (SUCCEEDED(hr)){
        hr = CMathInputControlEventHandler<CMIC_TEST_EVENTSDlg>::DispEventAdvise(m_spMIC);            
        if (SUCCEEDED(hr)){
          hr = m_spMIC->Show();  
        }
      }
    }
  }  
}
  
```



> [!Note]  
> El tipo de plantilla, CMIC TEST EventsDlg en este ejemplo, será diferente a menos que haya llamado a la clase igual \_ \_ que en el ejemplo.

 

 

 
