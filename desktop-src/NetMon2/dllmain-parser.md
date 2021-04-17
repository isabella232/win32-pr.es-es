---
description: La función de exportación de DllMain para el analizador identifica la existencia del analizador y libera los recursos que utiliza Monitor de red para el analizador. DllMain debe implementarse en todos los archivos dll de analizador.
ms.assetid: 2ce79d49-3aad-461f-99cf-cf632680efcc
title: Función de devolución de llamada del analizador DllMain (Process. h)
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667733"
---
# <a name="dllmain-parser-callback-function"></a>Función de devolución de llamada del analizador DllMain

La función de exportación de **DllMain** para el analizador identifica la existencia del analizador y libera los recursos que utiliza monitor de red para el analizador. **DllMain** debe implementarse en todos los archivos dll de analizador.

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

*hInstance* \[ de\]
</dt> <dd>

Identificador de una instancia del analizador.

</dd> <dt>

*Comando* \[ de\]
</dt> <dd>

Indicador para determinar por qué se llama a la función. Para obtener una lista de todas las marcas posibles, vea [DllMain](/windows/desktop/Dlls/dllmain). La implementación del analizador debe procesar los valores siguientes.



| Value                                                                                                                                                                         | Significado                                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DLL_PROCESS_ATTACH"></span><span id="dll_process_attach"></span><dl> <dt>**\_adjuntar proceso dll \_**</dt> </dl> | Cuando se llama a **DllMain** por primera vez, el archivo DLL debe llamar a [CreateProtocol](createprotocol.md) para proporcionar información monitor de red. <br/>   |
| <span id="DLL_PROCESS_DETACH"></span><span id="dll_process_detach"></span><dl> <dt>**desasociación de \_ procesos dll \_**</dt> </dl> | Cuando se llama a **DllMain** por última vez, el archivo DLL debe llamar a [DestroyProtocol](destroyprotocol.md) para liberar los recursos que utiliza el archivo dll. <br/> |



 

</dd> <dt>

*Reserved* 
</dt> <dd>

No se utiliza ahora.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El archivo DLL del analizador siempre devuelve **true**.

## <a name="remarks"></a>Observaciones

El sistema operativo llama a **DllMain** para cargar y descargar el archivo DLL del analizador. Esta función se basa en la función [DllMain](/windows/desktop/Dlls/dllmain) de la biblioteca de vínculos dinámicos.

También puede usar la implementación de **DllMain** para almacenar una instancia de un analizador para su uso en el futuro. Por ejemplo, puede almacenar una instancia de DLL de analizador y, a continuación, utilizarla para una llamada del sistema en el futuro.



| Para obtener información acerca de                                        | Vea                                                     |
|-----------------------------------------------------------|---------------------------------------------------------|
| Qué son los analizadores y cómo funcionan con Monitor de red. | [Analizadores](parsers.md)                                  |
| Qué puntos de entrada se incluyen en el archivo DLL del analizador.        | [Arquitectura de DLL de analizador](parser-dll-architecture.md)  |
| Cómo implementar **DllMain**  incluye un ejemplo.        | [Implementar DllMain](implementing-dllmain-parser.md) |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Process. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[CreateProtocol](createprotocol.md)
</dt> <dt>

[DestroyProtocol](destroyprotocol.md)
</dt> <dt>

[DllMain](/windows/desktop/Dlls/dllmain)
</dt> </dl>

 

