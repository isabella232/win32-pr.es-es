---
description: Crea un objeto de contexto que describe el dispositivo de tableta especificado.
ms.assetid: 76f48485-a958-4457-9b87-73de73fa671e
title: ITablet::CreateContext (método)
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
ms.openlocfilehash: 8b67e4c15d40f2da7a616295f10a7762b242fb40d9c0b5f42c00eb51d190cc03
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118450580"
---
# <a name="itabletcreatecontext-method"></a>ITablet::CreateContext (método)

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

*hWnd* \[ En\]
</dt> <dd>

Ventana a la que se adjuntará el contexto de la tableta.

</dd> <dt>

*prcInput* \[ En\]
</dt> <dd>

\[in, unique\]

Rectángulo de entrada de lápiz.

</dd> <dt>

*dwOptions* \[ En\]
</dt> <dd>

Marcas que establecen opciones de contexto de tableta.

</dd> <dt>

*pTCS* \[ En\]
</dt> <dd>

\[in, unique\]

Información detallada sobre el contexto de tableta que se creará.

</dd> <dt>

*cet* \[ En\]
</dt> <dd>

Valor que habilita o deshabilita los mensajes de contexto que se envían a la ventana.

</dd> <dt>

*ppCtx* \[ out\]
</dt> <dd>

Puntero al contexto de tableta recién creado.

</dd> <dt>

*pTcid* \[ in, out\]
</dt> <dd>

Valor que identifica de forma única la tableta.

</dd> <dt>

*ppPD* \[ in, out\]
</dt> <dd>

Puntero a información sobre los datos contenidos en cada paquete.

</dd> <dt>

*pSink* \[ En\]
</dt> <dd>

Objeto [**ITabletEventSink**](itableteventsink.md) donde se enviarán los mensajes de notificación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                            | Descripción                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | Correcto.<br/>                       |
| <dl> <dt>**E \_ FAIL**</dt> </dl> | Se ha producido un error no especificado.<br/> |



 

## <a name="remarks"></a>Comentarios

Normalmente, una aplicación obtiene los valores predeterminados del método [**ITablet::GetDefaultContextSettings**](itablet-getdefaultcontextsettings.md), modifica los valores para satisfacer sus necesidades y, a continuación, pasa la estructura de configuración modificada al método **ITablet::CreateContext**.

> [!Note]  
> Debe implementar la interfaz [**ITabletEventSink al**](itableteventsink.md) llamar al método **ITablet::CreateContext**.

 

El *parámetro dwOptions* es un conjunto de marcas de bits que describen las opciones de contexto. En la tabla siguiente se describen estas marcas.



| Nombre de marca                                | Valor                                                                                                                                                                                         | Descripción                                                                                                                                                                                                                                                              |
|------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| TCXO \_ MARGIN<br/>                  | 0x00000001<br/>                                                                                                                                                                         | Especifica que el contexto de entrada de la tableta tendrá un margen. El margen es un área fuera del área de entrada especificada donde los eventos se asignarán al borde del área de entrada. Esta característica facilita la entrada de puntos en el borde del contexto.<br/> |
| \_PREHOOK DE TCXO<br/>                 | 0x00000002<br/>                                                                                                                                                                         | El prehook obtiene paquetes antes de los contextos normales y los posthooks. Obtienen paquetes en el orden de creación.<br/>                                                                                                                                                  |
| ESTADO DEL \_ CURSOR \_ TCXO<br/>           | 0x00000004<br/>                                                                                                                                                                         | El TC devolverá paquetes incluso si el cursor está arriba. De forma predeterminada, un TC solo devolverá paquetes cuando el cursor esté fuera de servicio.<br/>                                                                                                                                       |
| TCXO \_ NO \_ CURSOR \_ DOWN<br/>        | 0x00000008<br/>                                                                                                                                                                         | El TC no devolverá paquetes cuando el cursor esté fuera de servicio.<br/>                                                                                                                                                                                                       |
| TCXO \_ NO \_ INTEGRADO<br/>         | 0x00000010<br/>                                                                                                                                                                         | El contexto no estará integrado.<br/>                                                                                                                                                                                                                           |
| TCXO \_ POSTHOOK<br/>                | 0x00000020<br/>                                                                                                                                                                         | Los posthooks obtienen paquetes después de los contextos de tableta normales, pero antes del contexto del sistema. Obtienen paquetes en el orden inverso de su creación.<br/>                                                                                                                   |
| TCXO \_ DONT \_ SHOW \_ CURSOR<br/>      | 0x00000080<br/>                                                                                                                                                                         | El TC no establecerá la posición del cursor.<br/>                                                                                                                                                                                                                      |
| TCXO \_ NO \_ VALIDA \_ TCS<br/>     | 0x00000100<br/>                                                                                                                                                                         | El TC no validará los GUID pasados en la configuración del contexto de la tableta con las propiedades admitidas del dispositivo.<br/>                                                                                                                                      |
| TCXO \_ ALLOW \_ FLICKS<br/>           | 0x00000400<br/>                                                                                                                                                                         | El TC permitirá que se lleve a cabo la detección de gestos (de forma predeterminada, esto solo se permite en contextos del sistema) y el cliente SE \_ eventos FLICK.<br/>                                                                                                               |
| TCXO \_ PERMITIR \_ \_ PULSACIONES DE COMENTARIOS<br/>   | 0x00000800<br/>                                                                                                                                                                         | La TC permitirá mostrar los comentarios del lápiz. De forma predeterminada, esto solo se permite en contextos del sistema.<br/>                                                                                                                                                              |
| TCXO \_ PERMITIR COMENTARIOS \_ SOBRE COMENTARIOS \_<br/> | 0x00001000<br/>                                                                                                                                                                         | La TC permitirá mostrar los comentarios del lápiz. De forma predeterminada, esto solo se permite en contextos del sistema.<br/>                                                                                                                                                              |
| TCXO \_ ALL<br/>                     | TCJO \_ MARGIN \| TCXO \_ PREHOOK \| TC TCXO CURSOR STATE TC TC \_ \_ \| TCXO NO CURSOR DOWN \_ \_ \_ \| \_ TCXO NON INTEGRATED \_ \| \_ TCHOOK \| TCJO \_ DONT SHOW CURSOR \_ \_ \| TCXO \_ DONT VALIDATE \_ \_ TCS<br/> | Todas las opciones de contexto de tableta definidas.<br/>                                                                                                                                                                                                                           |
| TCXO \_ HOOK<br/>                    | TCXO \_ PREHOOK \| TCXO \_ POSTHOOK<br/>                                                                                                                                                    | Combina la funcionalidad de enlace previo y posterior.<br/>                                                                                                                                                                                                                |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                          |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                              |
| Biblioteca<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**ITablet (interfaz)**](itablet.md)
</dt> <dt>

[**CONTEXT \_ ENABLE \_ TYPE (Enumeración)**](context-enable-type.md)
</dt> <dt>

[**Estructura DE \_ CONFIGURACIÓN DE CONTEXTO DE \_ TABLETA**](tablet-context-settings.md)
</dt> <dt>

[**ESTRUCTURA DE \_ DESCRIPCIÓN DE PAQUETES**](/windows/desktop/api/tpcshrd/ns-tpcshrd-packet_description)
</dt> <dt>

[**ITabletContextP (interfaz)**](itabletcontextp.md)
</dt> <dt>

[**ITabletEventSink (interfaz)**](itableteventsink.md)
</dt> </dl>

 

 




