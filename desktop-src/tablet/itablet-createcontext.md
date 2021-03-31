---
description: Crea un objeto de contexto que describe el dispositivo de tableta especificado.
ms.assetid: 76f48485-a958-4457-9b87-73de73fa671e
title: 'ITablet:: CreateContext (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet.CreateContext
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 9f1214f7f9e429b5f9b5b9614c2ccfc7fd1800b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912902"
---
# <a name="itabletcreatecontext-method"></a>ITablet:: CreateContext (método)

Crea un objeto de contexto que describe el dispositivo de tableta especificado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT CreateContext(
  [in]      HWND                    hWnd,
  [in]      RECT                    *prcInput,
  [in]      DWORD                   dwOptions,
  [in]      TABLET_CONTEXT_SETTINGS *pTCS,
  [in]      CONTEXT_ENABLE_TYPE     cet,
  [out]     ITabletContext          **ppCtx,
  [in, out] TABLET_CONTEXT_ID       *pTcid,
  [in, out] PACKET_DESCRIPTION      **ppPD,
  [in]      ITabletEventSink        *pSink
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hWnd* \[ de\]
</dt> <dd>

Ventana a la que se adjuntará el contexto de Tablet PC.

</dd> <dt>

*prcInput* \[ de\]
</dt> <dd>

\[en, único\]

Rectángulo de entrada manuscrita.

</dd> <dt>

*dwOptions* \[ de\]
</dt> <dd>

Marcas que establecen opciones de contexto de Tablet PC.

</dd> <dt>

*pTCS* \[ de\]
</dt> <dd>

\[en, único\]

Información detallada sobre el contexto de la tableta que se va a crear.

</dd> <dt>

*CET* \[ de\]
</dt> <dd>

Valor que habilita o deshabilita los mensajes de contexto que se envían a la ventana.

</dd> <dt>

*ppCtx* \[ enuncia\]
</dt> <dd>

Puntero al nuevo contexto de Tablet PC.

</dd> <dt>

*pTcid* \[ in, out\]
</dt> <dd>

Valor que identifica de forma única la tableta.

</dd> <dt>

*ppPD* \[ in, out\]
</dt> <dd>

Puntero a información acerca de los datos contenidos en cada paquete.

</dd> <dt>

*pSink* \[ de\]
</dt> <dd>

Objeto [**ITabletEventSink**](itableteventsink.md) en el que se enviarán los mensajes de notificación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                            | Descripción                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>   | Correcto.<br/>                       |
| <dl> <dt>**E \_ FAIL**</dt> </dl> | Se ha producido un error no especificado.<br/> |



 

## <a name="remarks"></a>Observaciones

Normalmente, una aplicación obtiene los valores predeterminados del [**método ITablet:: GetDefaultContextSettings**](itablet-getdefaultcontextsettings.md), modifica los valores para satisfacer sus necesidades y, a continuación, pasa la estructura de configuración modificada al **método ITablet:: CreateContext**.

> [!Note]  
> Debe implementar la [**interfaz ITabletEventSink**](itableteventsink.md) al llamar al **método ITablet:: CreateContext**.

 

El parámetro *dwOptions* es un conjunto de marcadores de bits que describen las opciones de contexto. En la tabla siguiente se describen estas marcas.



| Nombre de marca                                | Value                                                                                                                                                                                         | Descripción                                                                                                                                                                                                                                                              |
|------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_margen TCXO<br/>                  | 0x00000001<br/>                                                                                                                                                                         | Especifica que el contexto de entrada de la tableta tendrá un margen. El margen es un área fuera del área de entrada especificada en la que se asignarán los eventos al borde del área de entrada. Esta característica facilita la entrada de puntos en el borde del contexto.<br/> |
| PREENLACE TCXO \_<br/>                 | 0x00000002<br/>                                                                                                                                                                         | El PREENLACE obtiene los paquetes antes de los contextos y los postenlaces normales. Reciben paquetes en el orden en que se crean.<br/>                                                                                                                                                  |
| \_Estado de cursor de TCXO \_<br/>           | 0x00000004<br/>                                                                                                                                                                         | El TC devolverá los paquetes aunque el cursor esté activo. De forma predeterminada, un TC solo devolverá los paquetes cuando el cursor esté inactivo.<br/>                                                                                                                                       |
| TCXO \_ sin \_ cursor \_ inactivo<br/>        | 0x00000008<br/>                                                                                                                                                                         | El TC no devolverá los paquetes cuando el cursor esté inactivo.<br/>                                                                                                                                                                                                       |
| TCXO \_ no \_ integrado<br/>         | 0x00000010<br/>                                                                                                                                                                         | El contexto no estará integrado.<br/>                                                                                                                                                                                                                           |
| posthook de TCXO \_<br/>                | 0x00000020<br/>                                                                                                                                                                         | Los posthooks reciben paquetes después de los contextos de Tablet PC normales, pero antes del contexto del sistema. Reciben paquetes en el orden inverso a la creación.<br/>                                                                                                                   |
| TCXO \_ no \_ Mostrar \_ cursor<br/>      | 0x00000080<br/>                                                                                                                                                                         | El TC no establecerá la posición del cursor.<br/>                                                                                                                                                                                                                      |
| TCXO \_ no \_ validar \_ ect<br/>     | 0x00000100<br/>                                                                                                                                                                         | El TC no validará los GUID que se pasan en los valores de contexto de la tableta con las propiedades compatibles del dispositivo.<br/>                                                                                                                                      |
| TCXO \_ permitir \_ gestos<br/>           | 0x00000400<br/>                                                                                                                                                                         | El TC permitirá que se produzca la detección de gestos (de forma predeterminada, solo se permite en contextos del sistema) y el cliente obtendrá \_ los eventos de gestos.<br/>                                                                                                               |
| TCXO \_ permitir \_ \_ pulsaciones de comentarios<br/>   | 0x00000800<br/>                                                                                                                                                                         | El TC permitirá mostrar los comentarios del lápiz. De forma predeterminada, solo se permite en contextos del sistema.<br/>                                                                                                                                                              |
| TCXO \_ permitir \_ el \_ barril de comentarios<br/> | 0x00001000<br/>                                                                                                                                                                         | El TC permitirá mostrar los comentarios del lápiz. De forma predeterminada, solo se permite en contextos del sistema.<br/>                                                                                                                                                              |
| TCXO \_ todo<br/>                     | TCXO \_ margin \| TCXO \_ preenganchat \| TCXO \_ cursor \_ State \| TCXO not \_ \_ cursor \_ Down \| TCXO \_ \_ unintegrated \| TCXO \_ posthook \| TCXO no \_ \_ Show \_ cursor TCXO no \| \_ \_ validar \_ ect<br/> | Todas las opciones de contexto de Tablet PC definidas.<br/>                                                                                                                                                                                                                           |
| \_enlace TCXO<br/>                    | TCXO de \_ PREenlace de \| TCXO \_<br/>                                                                                                                                                    | Combina la funcionalidad de enlace previo y posterior al enlace.<br/>                                                                                                                                                                                                                |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/>                          |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                              |
| Biblioteca<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz ITablet**](itablet.md)
</dt> <dt>

[**\_Enumeración de tipo de habilitación de contexto \_**](context-enable-type.md)
</dt> <dt>

[**Estructura de configuración de \_ contexto de Tablet \_**](tablet-context-settings.md)
</dt> <dt>

[**Estructura de descripción de paquetes \_**](/windows/desktop/api/tpcshrd/ns-tpcshrd-packet_description)
</dt> <dt>

[**Interfaz ITabletContextP**](itabletcontextp.md)
</dt> <dt>

[**Interfaz ITabletEventSink**](itableteventsink.md)
</dt> </dl>

 

 




