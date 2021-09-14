---
description: La función de exportación DllMain para el analizador identifica la existencia del analizador y libera los recursos que Monitor de red usa para el analizador. DllMain debe implementarse en todos los archivos DLL del analizador.
ms.assetid: 2ce79d49-3aad-461f-99cf-cf632680efcc
title: Función de devolución de llamada del analizador de DllMain (Process.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DllMain
api_type:
- UserDefined
api_location:
- process.h
ms.openlocfilehash: 1db69d51f3a46bbe219ef7f7bdea67e8e8970e4d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127260444"
---
# <a name="dllmain-parser-callback-function"></a>Función de devolución de llamada del analizador de DllMain

La función de exportación **DllMain** para el analizador identifica la existencia del analizador y libera los recursos que Monitor de red usa para el analizador. **DllMain debe** implementarse en todos los archivos DLL del analizador.

## <a name="syntax"></a>Sintaxis


```C++
BOOL WINAPI DllMain(
  _In_ HANDLE hInstance,
  _In_ ULONG  Command,
       LPVOID Reserved
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hInstance* \[ En\]
</dt> <dd>

Identificador de una instancia del analizador.

</dd> <dt>

*Comando* \[ En\]
</dt> <dd>

Indicador para determinar por qué se llama a la función. Para obtener una lista de todas las marcas posibles, [vea DllMain](/windows/desktop/Dlls/dllmain). La implementación del analizador debe procesar los valores siguientes.



| Value                                                                                                                                                                         | Significado                                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DLL_PROCESS_ATTACH"></span><span id="dll_process_attach"></span><dl> <dt>**ASOCIACIÓN \_ DE PROCESOS DLL \_**</dt> </dl> | Cuando se llama a **DllMain** por primera vez, el archivo DLL debe llamar a [CreateProtocol](createprotocol.md) para proporcionar información a Monitor de red. <br/>   |
| <span id="DLL_PROCESS_DETACH"></span><span id="dll_process_detach"></span><dl> <dt>**\_DESASOCIÓN \_ DEL PROCESO DE DLL**</dt> </dl> | Cuando se llama a **DllMain** por última vez, el archivo DLL debe llamar a [DestroyProtocol](destroyprotocol.md) para liberar los recursos que usa el archivo DLL. <br/> |



 

</dd> <dt>

*Reserved* 
</dt> <dd>

No se usa ahora.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El archivo DLL del analizador siempre devuelve **TRUE.**

## <a name="remarks"></a>Observaciones

El sistema operativo llama **a DllMain** para cargar y descargar el archivo DLL del analizador. Esta función se basa en la función [DllMain](/windows/desktop/Dlls/dllmain) de la biblioteca de vínculos dinámicos.

También puede usar la implementación de **DllMain** para almacenar una instancia de un analizador para su uso en el futuro. Por ejemplo, puede almacenar una instancia dll del analizador y, a continuación, usarla para una llamada del sistema en el futuro.



| Para obtener información acerca de                                        | Vea                                                     |
|-----------------------------------------------------------|---------------------------------------------------------|
| Qué son los analizadores y cómo funcionan con Monitor de red. | [Analizadores](parsers.md)                                  |
| Qué puntos de entrada se incluyen en el archivo DLL del analizador.        | [Arquitectura dll del analizador](parser-dll-architecture.md)  |
| Cómo implementar **DllMain incluye**  un ejemplo.        | [Implementación de DllMain](implementing-dllmain-parser.md) |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Process.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[CreateProtocol](createprotocol.md)
</dt> <dt>

[DestroyProtocol](destroyprotocol.md)
</dt> <dt>

[DllMain](/windows/desktop/Dlls/dllmain)
</dt> </dl>

 

